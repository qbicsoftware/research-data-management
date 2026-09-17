# Sample batches

## What is a sample batch?

A sample batch is a group of samples shipped together to a measurement facility and processed under the same conditions. Tracking batches is how you identify and correct for **batch effects** — technical variation introduced when samples are processed at different times or under different conditions.

Undocumented batches are one of the most common causes of irreproducible results. [Learn more about batch effects](https://pmc.ncbi.nlm.nih.gov/articles/PMC3880143/).

## Creating and registering sample batches

1. In the experiment summary, click **Register sample batch**.

2. **Download the template** — an Excel spreadsheet with one row per sample.

    !!! note "Mandatory fields"
        Columns marked with an asterisk (`*`) are mandatory.

3. Fill in the template. For each sample, record its species, specimen, analyte, experimental group, and any other required details.

    !!! tip "Sample IDs are assigned automatically"
        Don't fill in the Sample ID column. The system generates a unique, permanent ID for each sample (e.g. `Q2ABCD001AA`) when you register the batch.

4. Upload the completed file in the registration dialog. The system validates it and highlights any errors.

5. Enter a **batch name** (e.g. "Pilot cohort — January 2026").

6. Click **Register**. The system processes your samples in the background.

7. Click **Finish** when done.

!!! info "Email notification"
    All [project collaborators](../project/project_access.md#add-collaborator) receive an email with a link to the new batch.

??? info "Sample ID format"
    Sample IDs follow the pattern `Q2XXXXNNNCC`: the six-character project code, a three-digit running number, and a two-character random suffix (e.g. `Q2ABCD001AA`). They are permanent and cannot be changed after registration.

## Editing sample batches

You can update sample metadata after registration. You cannot add or remove individual samples from a batch.

1. Click the **edit** button next to the batch.

    !!! info "Required role"
        You need **write** or **admin** role.

2. **Download the current metadata** — the template is pre-filled with existing values.

3. Make your changes. Grey columns (e.g. `Sample Id`) are locked — changes there are ignored.

    !!! note "Mandatory fields"
        Columns marked with `*` remain mandatory.

4. Upload the edited file, optionally rename the batch, and click **Edit batch**.

5. Click **Finish**.

## Deleting a sample batch

!!! danger "This is irreversible"
    Deleting a batch permanently removes all sample metadata for every sample in that batch.

!!! warning "Measurements must be removed first"
    A batch can only be deleted if none of its samples are referenced by a measurement. [Delete the measurements](../measurement/measurement_edit.md#delete-measurements) first.

1. Click the **delete** button next to the batch.

    !!! info "Required role"
        You need **write** or **admin** role.

2. Click **Confirm** in the dialog.

## Download sample metadata

Click **Download sample metadata** to export all registered sample metadata as an `.xlsx` file. This is useful for copying sample IDs into [measurement registration spreadsheets](../measurement/measurement_registration.md).

---

## What's next

➡ [Register measurements](../measurement/measurement_registration.md)
