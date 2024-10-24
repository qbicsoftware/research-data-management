# Sample Batch
[//]: # (What is a sample batch?)
## Definition

A sample batch forms a logical container of samples that are going to be shipped together to the
measurement facility with the intention of being processed under the same conditions.

[//]: # (What is the purpose of grouping samples into batches?)
## Intention 

Grouping and processing samples as distinct sample batches is key in properly tracking and avoiding batch effects.
Click [here](https://pmc.ncbi.nlm.nih.gov/articles/PMC3880143/) for a quick introduction into batch effect and their impact on research data. 

[//]: # (How do I add samples to my experiment?)
## Creating and registering sample batches

We call the process of adding samples to an experiment "sample registration". 
When you want to link samples to an experiment you need to register metadata for those samples.

To **start** with the sample registration process, click on the button `Register sample batch` to open the sample registration dialog.

Please go ahead and **download the metadata template file** from the dialog.
In this file you can fill out information for the samples you want to register. 

!!! note
    **Mandatory** information for the sample registration is marked by an asterix `*` after the column name.

**Once you filled out** all the information, you can go back to the dialog. In case you closed the dialog, simply re-open it.
</br>
Please go ahead and **upload your filled metadata file** in the dialog.
Once the data manager validated the information in your file,
go ahead and **choose a name for your batch**.
</br>
Once you named your batch and uploaded the file with the necessary information, go ahead and **click the
`Register`** button. The data manager will now go through the process of creating samples within your
experiment.

!!! info "Email Notification"
    Upon successful batch registration,
    all [project collaborators](../project/project_access.md#add-collaborator) will automatically receive
    an email with a link to the created batch.

After the data manager is done registering your samples, you can **close** the dialog **by clicking the
`Finish`** button.
Now samples annotated with the provided metadata are registered to your experiment. You can see the
newly created batch next to the other batches in the samples view.

!!! info "SampleId"
    Upon successful batch registration, each sample will be associated with a unique SampleId 
    distinguishing it from other samples within the system
    an email with a link to the created batch.

[//]: # (How do I edit existing samples in my experiment?)
## Editing sample batches

You might need to edit sample metadata after registering the sample batch to the experiment.
Editing sample information is restricted to editing the sample metadata. Adding or removing samples from a batch is not possible.

To **start** with the sample edit process, click on the edit button next to the batch you want to edit. This will open the batch editing dialog.

!!! info "Project role"
    Should you not see the action column,   
    please make sure that you have been granted the "write" or "admin" role to it by the project owner/admin.

Please go ahead and **download the metadata template file** from the dialog.
In this file you can fill out information for the samples you want to register. 

!!! note
    **Mandatory** information for the sample editing is marked by an asterix `*` after the column name.

Note that the information in greyed out columns such as e.g. `Sample Id` is immutable and changes made within will not be registered during the sample editing process.

!!! note
    Information shown in greyed out columns are immutable and cannot be changed. 

**Once you filled out** all the information, you can go back to the dialog. In case you closed the dialog, simply re-open it.
</br>
Please go ahead and **upload your filled metadata file** in the dialog.
Once the data manager validated the information in your file,
go ahead and **choose a name for your batch** if you want to change it.
</br>
Once you named your batch and uploaded the file with the necessary information, go ahead and **click the
`Edit batch`** button. The data manager will now go through the process of updating the sample information within your
experiment.

After the data manager is done registering your samples, you can **close** the dialog **by clicking the
`Finish`** button.

[//]: # (How do I delete existing samples in my experiment?)
## Delete a sample batch

!!! warning "Batch Deletion"
    Keep in mind, that deleting a batch will also delete all sample metadata of the samples within the batch

To **start** with the sample batch deletion process, click on the **`delete`** button next to the batch in question within the action column.

!!! info "Project role"
    Should you not see the action column,   
    please make sure that you have been granted the "write" or "admin" role to it by the project owner/admin.

This will open the batch deletion dialog requiring **confirmation** of the batch deletion process by clicking the **`Confirm`** button.

!!! warning "Attached Measurements"
    Keep in mind, that batches can only be deleted if none of the samples within the batch have been used in a measurement.)
    Otherwise, you need to delete the measurements in question before the batch can be deleted.

[//]: # (How do I download sample metadata)
## Download sample metadata

To **download** the sample metadata for all registered samples click on the **`Download sample metadata`** button.
This will export the provided registered metadata as an `.xlsx` file to your local download directory.
