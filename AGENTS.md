# AGENTS.md

> This file describes the AI agent system used to generate documentation proposals in this repository. All agents are configured in `opencode.json`. Generated proposals live in `docs/proposals/` and require human review before adoption.

---

## Overview

Documentation in this repository is generated through a structured multi-agent debate. Rather than having a single AI write documentation in one pass, four specialist agents each contribute their perspective, challenge one another's drafts, and a fifth editorial agent unifies the result into a single coherent voice.

The goal is documentation that is simultaneously **accurate**, **reproducible**, **accessible**, and **readable** — without any single perspective dominating at the expense of the others.

---

## How It Works

Every documentation request runs through four rounds:

**Round 1 — Independent Drafts**
The four subject-matter agents each write a draft independently, without seeing each other's work. This ensures each perspective is genuinely uninfluenced before the debate begins.

**Round 2 — Cross-Review**
Each agent reviews the other three drafts and returns specific, cited challenges: factual corrections, compliance gaps, accessibility problems, and concrete rewrite proposals. Vague criticism is not accepted — every challenge must include a suggested fix.

**Round 3 — Consensus Synthesis**
The `docs` orchestrator reconciles all four drafts and the Round 2 challenges into a single consensus document. Where agents disagree, the orchestrator applies a clear precedence order (see below) and records its reasoning in a `## Debate Summary` section at the top of every proposal.

**Round 4 — Editorial Pass**
The `technical-editor` agent receives the reconciled draft and performs a final pass focused entirely on voice, flow, and readability — without touching any factual content. This is the step that ensures the output reads as one coherent document rather than a committee report.

The final file is written to `docs/proposals/<document-name>.md` and marked as a proposal pending human review.

---

## Agent Roles

### `docs` — Orchestrator
**Model**: claude-opus-4-6
**Role**: Routes requests, manages the four debate rounds, synthesises consensus, and writes the final proposal to `docs/proposals/`.

The orchestrator never writes documentation itself during the debate. Its job is coordination, conflict resolution, and final synthesis. It is the only agent with write access, and that access is restricted exclusively to `docs/proposals/`.

**Conflict precedence order** (applied during Round 3 synthesis):
1. Compliance and FAIR accuracy → `data-steward` challenges take precedence
2. Computational and provenance accuracy → `bioinformatician` challenges take precedence
3. Plain-language accessibility → `lab-personnel` challenges take precedence
4. Structure and platform navigability → `ls-user-guide` challenges take precedence

---

### `data-steward` — Compliance & Metadata Accuracy
**Model**: claude-sonnet-4-6
**Voice in the debate**: *"Is this FAIR-compliant and correctly annotated?"*

The data steward is the compliance firewall. It ensures that data and metadata descriptions conform to domain-specific schemas, controlled vocabularies, and Open Science regulations. It holds the line on accuracy — no compliance gap passes through without a citation and a correction.

**Domain coverage**:
- Genomics: FASTQ, BAM/CRAM, VCF; EGA, SRA, ENA submission standards
- Proteomics: mzML/mzXML, mzIdentML; PRIDE/ProteomeXchange requirements
- Immunopeptidomics: HLA-peptidomics, PSMs, MHC ligandome metadata, IEDB schemas
- Imaging: OME-TIFF, CZI, DICOM, Visium; BioImage Archive and REMBI standards

**Key standards enforced**: FAIR principles, OBO Foundry, EFO, NCIT, PSI-MS, MIAME, MINSEQE, REMBI, Plan S, Horizon Europe DMP, NIH DMSP

---

### `lab-personnel` — Bench Scientist / PI Perspective
**Model**: claude-sonnet-4-6
**Voice in the debate**: *"Can a bench scientist actually follow this?"*

This agent represents the primary documentation consumer: a PI or wet-lab scientist with deep biological expertise but little data management background. It advocates for plain language, short steps, and everyday analogies. If a section would cause a busy scientist to disengage, this agent flags it and proposes a simpler alternative.

**What it protects against**: unexplained acronyms, jargon-heavy compliance language, walls of text, steps that feel disconnected from daily lab workflow, and documentation that respects the data manager more than the scientist reading it.

---

### `bioinformatician` — Computational Provenance & Pipeline Accuracy
**Model**: claude-sonnet-4-6
**Voice in the debate**: *"Is the computational provenance chain correctly and reproducibly described?"*

This agent fills the gap between compliance metadata and computational reality. It ensures that documentation correctly describes how derived data traces back to primary data — including software versions, parameter sets, checksums, workflow execution records, and environment specifications. If a described workflow would be non-reproducible as written, this agent catches it.

**Domain coverage**:
- Genomics pipelines: FastQC, STAR, BWA-MEM2, GATK, Salmon, Nextflow, Snakemake
- Proteomics pipelines: MaxQuant, MSFragger, Spectronaut, DIA-NN, Perseus, MSstats
- Immunopeptidomics: OptiType, HLA-HD, PSM-level filtering criteria
- Imaging analysis: ilastik, CellProfiler, QuPath, Cellpose

**Key standards**: FAIR4RS, Workflow RO-Crate, CWL/WDL metadata

---

### `ls-user-guide` — Platform Structure & Navigation
**Model**: claude-haiku-4-5-20251001
**Voice in the debate**: *"Is this well-structured and does it hold together as a platform guide?"*

This agent sits at the intersection of the other three. It ensures documentation is grounded in actual platform UI steps and navigation paths, clearly distinguishes required from optional fields, and proposes bridge language when the other three agents are pulling in different directions. It is also the agent most likely to catch structural seams — places where the document stops flowing naturally.

**What it protects against**: vague platform references, inconsistent field labelling, missing callouts for common mistakes, and logical gaps that would send a user looking elsewhere for help.

---

### `technical-editor` — Voice & Readability
**Model**: claude-sonnet-4-6
**Role**: Round 4 post-synthesis editorial pass — not a debate participant.

The technical editor never participates in the debate. It receives only the final reconciled consensus draft and performs one job: making it read like it was written by one thoughtful human, not assembled by a committee.

**Target register**: Conversational but professional — precise and confident without being stiff, friendly without being patronising. Think Notion's help docs or a well-edited Nature Methods protocol.

**What it fixes**:
- Tonal whiplash between sections written in different registers
- Passive voice, hedging language, and throat-clearing openers
- AI-characteristic patterns: overly balanced constructions, unnaturally complete enumerations, hollow transitions
- Inconsistent formatting of UI elements, field labels, and callout styles
- Sentence rhythm — deliberately varying length so the text reads as human

**What it never changes**: factual content, compliance requirements, tool names, standard citations, the Debate Summary, or the proposal warning header.

---

## Output Format

Every generated file in `docs/proposals/` follows this structure:

```
> ⚠️ PROPOSAL — Pending review and approval before adoption.

## Debate Summary
[Key conflicts between agents and orchestrator tie-break reasoning]

---
[Document content]
```

The Debate Summary is intentionally preserved in the final output. It gives human reviewers full visibility into where the agents disagreed and why a particular position was chosen — making the review process faster and more informed.

---

## Permissions & Write Access

| Agent | Write access | Editable paths |
|---|---|---|
| `docs` (orchestrator) | ✅ Yes | `docs/proposals/` only |
| `data-steward` | ❌ No | — |
| `lab-personnel` | ❌ No | — |
| `bioinformatician` | ❌ No | — |
| `ls-user-guide` | ❌ No | — |
| `technical-editor` | ❌ No | — |

No subagent can write, edit, or overwrite any file in the repository. Only the orchestrator can write, and only to `docs/proposals/`. Existing files are never overwritten — a version suffix (e.g. `-v2`) is appended if a filename already exists.

---

## Extending the System

**Adding a new agent perspective**: Define the new agent in `opencode.json` with `"write": false, "edit": false`. Update the orchestrator's `permission.task` block to include it, add it to Rounds 1 and 2 in the orchestrator prompt, and document it here.

**Adding a new omic modality**: Update the `data-steward` and `bioinformatician` prompts in `opencode.json` with the relevant file formats, metadata standards, and pipeline tools. No structural changes to the debate protocol are needed.

**Changing the editorial register**: Update the `technical-editor` prompt's target register description and reference points. The rest of the pipeline is unaffected.

---

*This file is maintained manually. When the agent configuration in `opencode.json` changes, update this file to reflect the change.*
