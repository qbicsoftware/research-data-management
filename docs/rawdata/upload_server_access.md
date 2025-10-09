# Request Access as a data submitter

This section gives an overview on how to submit data as an external party.

!!! tip
    Should you be a member of the university of Tübingen you can immediately [upload your data](raw_data_upload.md) and skip this process.

## Procedure

Access to our upload server from outside the university network requires an explicit whitelisting of the uploader IP address as well as user authentication using strong cryptographic keys.
When requesting access to upload the data, please tell us your name and affiliation. We require a public and static IP address from the machine you will connect from for the purpose of granting access to the upload server. Please check with your IT department how to obtain such an IP address.
Your request should be sent to [support@qbic.zendesk.com](mailto:support@qbic.zendesk.com)

### Generate a key

For account creation a public key is required. Please generate a key as described below.

=== "Linux"

    Open your terminal and execute the following command and replace the email address with yours
    ``` bash
    ssh-keygen -t ed25519 -a 420 -f ~/.ssh/qbic-upload.ed25519 -C "your_email@example.com"
    ```

=== "MacOS"

    Open Terminal [as described by Apple](https://support.apple.com/guide/terminal/open-or-quit-terminal-apd5265185d-f365-44cb-8b09-71a064a42125/mac) and replace the email address with yours
    ``` bash
    ssh-keygen -t ed25519 -a 420 -f ~/.ssh/qbic-upload.ed25519 -C "your_email@example.com"
    ```

=== "Windows"

    Open PowerShell [as described by Microsoft](https://learn.microsoft.com/en-us/powershell/scripting/windows-powershell/starting-windows-powershell?view=powershell-7.5#run-from-the-start-menu) and replace the email address with yours
    ``` bash
    ssh-keygen -t ed25519 -a 420 -f $HOME/.ssh/qbic-upload.ed25519 -C "your_email@example.com"
    ```

Now you have a key with the name `qbic-upload.ed25519` and a public key named `qbic-upload.ed25519.pub`.

### Email us the required information

After you have generated your key and found out your IP address, send us a request for access to the upload server.
Please write an email to [support@qbic.zendesk.com](mailto:support@qbic.zendesk.com) and attach the public (.pub) key file.
!!! warning 
    Make sure you send us the public key ending with .pub 

    **Do not send us the private key!**

```txt
Dear QBiC Team

I would like to upload measurement data to your data manager. 
Can you please provide me with an account on your upload server. 

These are the required information:

Name: Max Mustermann
E-Mail: max.mustermann@example.com
Affiliation: My Research Institute, Berlin
IP-Address: <Your static public IPV4 Adress>

For accessing your upload server I would like to use the attached key.

Attachments: qbic-upload.ed25519.pub
```

### Wait for a reply
After we received the required information, we will create an account on our upload server. You will receive an email with a confirmation and the assigned username.

!!! note 
    Please note down the username as this will be the username you will use to connect to the upload server.

### Proceed by [uploading data](raw_data_upload.md)
