# Sample Batch
[//]: # (What is a sample batch?)
## Definition

A sample batch forms a logical container of samples that are going to be shipped together to the
measurement facility to get analysed.

[//]: # (TODO Why do we use this concept?)

[//]: # (How do I add samples to my experiment?)
## Creating and registering sample batches

We call the process of addind samples to an experiment sample registration. When you want to link
samples to an experiment you need to register some metadata for those samples.

To **start** with the sample registration, click on the button `Register sample batch`. A dialog will open.

Please go ahead and **download the metadata template file** from the dialog.
In this file you can fill out information for the samples you want to register. 

!!! note
    **Mandatory** information for the sample registration is marked by an asterix `*` after the column name.

**Once you filled out** all the information, you can go back to the dialog. In case you closed the dialog, simply re-open it again.
</br>
Please go ahead and **upload your filled metadata file** in the dialog.
Once the data manager validated the information in your file,
go ahead and **choose a name for your batch**.
</br>
Once you named your batch and uploaded the file with the necessary information, go ahead and **click
`Register`**. The datamanager will now go through the process of creating samples within your
experiment.

!!! info "Email Notification"
    Upon successful batch registration,
    all [project collaborators](../project/project_access.md#add-collaborator) will automatically receive
    an email with a link to the created batch.

After the data manager is done registering your samples, you can **close** the dialog **by clicking
`Finish`**.
Now samples annotated with the provided metadata are registered to your experiment. You can see the
newly created batch next to the other batches in the samples view.


[//]: # (How do I edit existing samples in my experiment?)
## Editing sample batches

You might need to edit sample metadata after registering the sample batch to the experiment.
Editing sample information is restricted to editing the sample metadata. Adding or removing samples from a batch is not possible.

To **start** with the sample registration, click on the edit button next to the batch you want to edit. A dialog will open.

Please go ahead and **download the metadata template file** from the dialog.
In this file you can fill out information for the samples you want to register. Columns that are
greyed out are not supposed to be changed by you.

!!! note
    Information in greyed out columns should not be changed by you.
!!! note
    **Mandatory** information for the sample editing is marked by an asterix `*` after the column name.

**Once you filled out** all the information, you can go back to the dialog. In case you closed the dialog, simply re-open it again.
</br>
Please go ahead and **upload your filled metadata file** in the dialog.
Once the data manager validated the information in your file,
go ahead and **choose a name for your batch** if you want to change it.
</br>
Once you named your batch and uploaded the file with the necessary information, go ahead and **click
`Edit batch`**. The datamanager will now go through the process of updating the sample information within your
experiment.

After the data manager is done registering your samples, you can **close** the dialog **by clicking
`Finish`**.

[//]: # (TODO How do I delete sample batches from my experiment?)
## Delete a sample batch

[//]: # (TODO How do I download sample metadata)
## Download sample metadata

[//]: # ()
[//]: # (From within your experiment, navigate to the `Register Sample Batch` step as described in )

[//]: # (Start by [navigating]&#40;../project/project_introduction.md#project-navigation&#41; to the project summary view of your project of interest.)

[//]: # ([Navigate]&#40;../experiment/experiment_introduction.md#experiment-navigation&#41; into the experiment of interest and within the experiment [navigate]&#40;#batch-navigation&#41; into the batch summary view.)

[//]: # (Within this view you are able to [register]&#40;batch_registration.md&#41; or [edit]&#40;batch_edit.md&#41; your sample batches.)

[//]: # ()
[//]: # (## Batch Navigation)

[//]: # ()
[//]: # (From the experiment summary you can navigate into the batch summary view.)

[//]: # (To do so, click on the "register sample batch" tab within the experiment navigation bar on the top.)

[//]: # (![experiment_summary.png]&#40;../experiment/images/experimental_summary.png&#41;)

[//]: # (This will take you to the batch summary view)

[//]: # (![batch_summary]&#40;images/batch_summary_no_batches.png&#41;)

[//]: # ()
[//]: # (# Batch Registration)

[//]: # ()
[//]: # (To register a new batch, start by [navigating]&#40;batch_introduction.md#batch-navigation&#41;)

[//]: # (into the batch summary view.)

[//]: # (![batch_summary]&#40;images/batch_summary_no_batches.png&#41;)

[//]: # ()
[//]: # (!!! info "Email Notification")

[//]: # (Upon successful batch registration, all [project collaborators]&#40;../project/project_access.md#add-collaborator&#41;)

[//]: # (will automatically receive an email with a link to the created batch.)

[//]: # ()
[//]: # (Within this view, click on the register button within the batch registration component on the top right to)

[//]: # (trigger the batch registration dialog.)

[//]: # (![batch_registration_dialog]&#40;images/batch_registration_dialog.png&#41;)

[//]: # ()
[//]: # (Within this dialog you have the possibility to provide the minimal required batch and sample information.)

[//]: # ()
[//]: # (The minimal batch information consists of:)

[//]: # ()
[//]: # (1. Batch name)

[//]: # (2. The [sample metadata information]&#40;#sample-registration&#41; for at least one sample.)

[//]: # ()
[//]: # (## Sample Registration)

[//]: # ()
[//]: # (The sample specific mandatory metadata information has to be defined within the spreadsheet of the dialog.)

[//]: # (Each row within this spreadsheet represents one sample within your batch.)

[//]: # (You can add or remove rows via the dedicated control buttons on top right of the spreadsheet.)

[//]: # (For a high amount of samples, we recommend to click on the "Prefill spreadsheet" button)

[//]: # (to trigger an automatic prefilling of the spreadsheet with the information provided during [experiment creation]&#40;../experiment/experiment_creation.md&#41;)

[//]: # ()
[//]: # (!!! tip "Prefill Sample Information")

[//]: # (The "Prefill Spreadsheet" functionality will generate one row each according to the number of biological replicates and conditions defined during)

[//]: # ([experimental group creation]&#40;../experiment/experiment_creation.md#experimental-group-creation&#41;.)

[//]: # ()
[//]: # (Mandatory metadata properties can be recognized via the asterisk next to the column header and consist of:)

[//]: # ()
[//]: # (1. Analysis to be performed)

[//]: # (2. Sample Label)

[//]: # (3. Condition)

[//]: # (4. Species)

[//]: # (5. Specimen)

[//]: # (6. Analyte)

[//]: # ()
[//]: # (!!! note "Preselected Information")

[//]: # (Cells within the "Species", "Specimen" and "Analyte" columns provide the values specified during [experiment creation]&#40;../experiment/experiment_creation.md&#41;. They can be automatically prefilled, if only one species, specimen, analyte was chosen, respectively.)

[//]: # (Cells within the "Condition" column provide a selection of the values specified during [experimental group creation]&#40;../experiment/experiment_creation.md#experimental-group-creation&#41;)

[//]: # ()
[//]: # (Optionally, feel free to also store a comment of your choosing and an Organism ID properties for each sample.)

[//]: # ()
[//]: # (![batch_registration_dialog_filled.png]&#40;images/batch_registration_dialog_filled.png&#41;)

[//]: # ()
[//]: # (Once all the required information has been provided you can trigger the sample batch registration via the "Register")

[//]: # (button below, which will register the metadata information for your batch in our system.)

[//]: # ()
[//]: # (!!! note "Sample ID")

[//]: # (During batch registration each sample will be provided a unique Sample ID,)

[//]: # (distinguishing it from other samples within the system.)

[//]: # ()
[//]: # (The batch information for each batch is shown in the top right batch component, while the sample specific information is shown in the grid of the center sample component.)

[//]: # (![batch_summary_with_batch.png]&#40;images/batch_summary_with_batch.png&#41;)

[//]: # ()
[//]: # (Should you notice any issues with your registered batches, you can always [edit]&#40;batch_edit.md&#41; or [delete]&#40;batch_edit.md#batch-deletion&#41;)

[//]: # (via their respective icons within the action column of grid in the batch component.)

[//]: # ()
[//]: # (## Batch Metadata Download)

[//]: # ()
[//]: # (You can download the sample specific metadata via the download metadata button on the right within the sample component, which will provide the metadata as a tab seperated *.txt file.)

[//]: # (![batch_registration_downloaded_metadata.png]&#40;images/batch_registration_downloaded_metadata.png&#41;)

[//]: # ()
[//]: # (# Batch Edit)

[//]: # ()
[//]: # ([//]: # &#40;TODO&#41;)
[//]: # ()
[//]: # (To edit the information of a batch, start by [navigating]&#40;batch_introduction.md#batch-navigation&#41;)

[//]: # (into the batch summary view.)

[//]: # (![batch_summary]&#40;images/batch_summary_with_batch.png&#41;)

[//]: # (Within this view, click on the edit icon &#40;pen symbol&#41; within the action column of the grid in the batch component)

[//]: # (to open the edit batch dialog.)

[//]: # (![batch_edit_dialog]&#40;images/batch_edit_dialog.png&#41;)

[//]: # ()
[//]: # (!!! info "Project role")

[//]: # (Should you not see the action column,)

[//]: # (please make sure that you have been granted the "write" or "admin" role to it by the project owner/admin!)

[//]: # ()
[//]: # (Once the dialog has been opened you can edit the sample or batch attributes of interest.)

[//]: # (![batch_edit_dialog_edited]&#40;images/batch_edit_dialog_edited.png&#41;)

[//]: # ()
[//]: # (Since each row within this spreadsheet represents one sample within your batch you can also add or remove)

[//]: # (samples via the dedicated control buttons on top right of the spreadsheet.)

[//]: # ()
[//]: # (Finally, save your changes via the "Save" button on the bottom of the dialog.)

[//]: # (![batch_edit_summary_edited.png]&#40;images/batch_edit_summary_edited.png&#41;)

[//]: # ()
[//]: # (## Batch Deletion)

[//]: # ()
[//]: # (!!! warning "Batch Deletion")

[//]: # (Keep in mind, that deleting a batch will also delete all sample metadata of the samples within the batch.)

[//]: # (If you want to delete individual sample metadata entries, remove the sample specific row via the [batch edit]&#40;#batch-edit&#41; functionality.)

[//]: # ()
[//]: # (To delete a batch, start by [navigating]&#40;#batch-navigation&#41;)

[//]: # (into the batch summary view.)

[//]: # (![batch_deletion_summary]&#40;images/batch_deletion_summary.png&#41;)

[//]: # ()
[//]: # (Within this view, click on the delete icon &#40;trashcan symbol&#41; within the action column of the grid in the batch component)

[//]: # (which will open up a dialog requiring validation of the batch deletion.)

[//]: # (![batch_deletion_triggered]&#40;images/batch_deletion_triggered.png&#41;)

[//]: # ()
[//]: # (!!! info "Project role")

[//]: # (Should you not see the action column,)

[//]: # (please make sure that you have been granted the "write" or "admin" role to it by the project owner/admin!)

[//]: # ()
[//]: # (Press the "Confirm" button to trigger the batch deletion.)

[//]: # (![batch_deletion_triggered]&#40;images/batch_deletion_successful_summary.png&#41;)

[//]: # ()
[//]: # (!!! info "Attached Measurements")

[//]: # (Keep in mind, that batches can only be deleted if none of the samples within the batch have been used in a measurement.)

[//]: # (Otherwise, you need to delete the measurement before the batch can be deleted.)
