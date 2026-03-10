# Confounding variables

A confounding variable is something you didn't control in your experiment but that might still affect your results — the time of day samples were collected, which lab member processed them, or whether a reagent lot changed mid-experiment. Recording these factors lets you account for them during analysis.

!!! info "Why this matters"
    *"Confounding occurs when an investigator tries to determine the effect of an exposure on the occurrence of a disease (or other outcome), but then actually measures the effect of another factor."*
    — Jager et al. (2008), *Kidney International*, 73(3), 256–260. [DOI](https://doi.org/10.1038/sj.ki.5002650)

Confounding variables are defined per experiment and cannot currently be shared across experiments.

## Define a confounding variable

Navigate to your experiment and locate the confounding variables section. Add a variable by providing its name (e.g. `Collection time`, `Operator`, `Passage number`).

## Assign values to samples

After defining variables, annotate individual samples during [batch registration](../batch/sample-batch.md#creating-and-registering-sample-batches) or [batch editing](../batch/sample-batch.md#editing-sample-batches). Not every sample needs a value — fill in only what you observed.

## Rename a variable

Open the confounding variables editing controls, enter the new name, and save. Existing sample values are preserved.

## Delete a variable

!!! danger "This is irreversible"
    Deleting a confounding variable permanently removes **all values assigned to that variable across every sample in the experiment**. Export your [sample metadata](../batch/sample-batch.md#download-sample-metadata) first if you need a record.

---

## What's next

➡ [Register sample batches](../batch/sample-batch.md)
