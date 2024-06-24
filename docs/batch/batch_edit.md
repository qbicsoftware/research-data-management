# Batch Edit

To edit the information of a batch, start by [navigating](batch_introduction.md#batch-navigation)
into the batch summary view.
![batch_summary](images/batch_summary_with_batch.png)
Within this view, click on the edit icon(pen symbol) within the action column of the grid in the batch component
to open the edit batch dialog.
![batch_edit_dialog](images/batch_edit_dialog.png)

!!! info "Project role"
    Should you not see the action column,
    please make sure that you have been granted the "write" or "admin" role to it by the project owner/admin!

Once the dialog has been opened you can edit the sample or batch attributes of interest.
![batch_edit_dialog_edited](images/batch_edit_dialog_edited.png)

Since each row within this spreadsheet represents one sample within your batch you can also add or remove 
sample specific metadata via the dedicated control buttons on top right of the spreadsheet.

Finally, save your changes via the "Save" button on the bottom of the dialog. 
![batch_edit_summary_edited.png](images/batch_edit_summary_edited.png)

## Batch Deletion

!!! warning "Batch Deletion"
    Keep in mind, that deleting a batch will also delete all sample metadata of the samples within the batch.
    If you want to delete individual sample metadata entries, remove the sample specific row via the [batch edit](#batch-edit) functionality.

To delete a batch, start by [navigating](batch_introduction.md#batch-navigation)
into the batch summary view.
![batch_deletion_summary](images/batch_deletion_summary.png)

Within this view, click on the delete icon(trashcan symbol) within the action column of the grid in the batch component
which will open up a dialog requiring validation of the batch deletion trigger. 
![batch_deletion_triggered](images/batch_deletion_triggered.png)

!!! info "Project role"
    Should you not see the action column,
    please make sure that you have been granted the "write" or "admin" role to it by the project owner/admin!

Press the "Confirm" button to trigger the batch deletion. 
![batch_deletion_triggered](images/batch_deletion_successful_summary.png)

!!! info "Attached Measurements"
    Keep in mind, that batches can only be deleted if none of the samples within the batch have been used in a measurement.
    Otherwise, you need to delete the measurement before the batch can be deleted.
