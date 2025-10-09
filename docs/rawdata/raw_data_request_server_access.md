# Request Server Access

This section gives an overview on how to request access to our upload server to submit data from outside of the University Tübingen network.

!!! tip
    Should you be a member of the university of Tübingen you can immediately [upload your data](raw_data_upload.md) and skip this process.

## Prerequisites

- An `ed25519` encrypted public and private keypair on the connecting machine
- The static and public `IPv4` address of the connecting machine
- The name and affiliation of the data submitting party

## Procedure

To minimize security risk. access to our upload server is restricted to temporary whitelisted IP addresses from outside of the university network.
!!! note
    Please make sure to provide a **public** and **static** IP address from the machine you want to connect from.
    Check with your IT department on details on how to obtain such an IP address.

As an additional security layer, data submitters have to authenticate using [strong cryptographic keys](#generate-cryptographic-keys).
Once these technical details are resolved, feel free to contact us to [request access to our server](#get-in-contact)

### Generate Cryptographic Keys

For account creation a public key is required. Please generate an ssh keypair via your system specific command and make sure to specify your email address:

=== "Linux"

    Open your terminal
    ``` bash
    ssh-keygen -t ed25519 -a 420 -f ~/.ssh/qbic-upload.ed25519 -C "<your_email@example.com>"
    ```

=== "MacOS"

    Open Terminal [as described by Apple](https://support.apple.com/guide/terminal/open-or-quit-terminal-apd5265185d-f365-44cb-8b09-71a064a42125/mac)
    ``` bash
    ssh-keygen -t ed25519 -a 420 -f ~/.ssh/qbic-upload.ed25519 -C "<your_email@example.com>"
    ```

=== "Windows"

    Open PowerShell [as described by Microsoft](https://learn.microsoft.com/en-us/powershell/scripting/windows-powershell/starting-windows-powershell?view=powershell-7.5#run-from-the-start-menu)
    ``` bash
    ssh-keygen -t ed25519 -a 420 -f $HOME/.ssh/qbic-upload.ed25519 -C "<your_email@example.com>"
    ```

with the name `qbic-upload.ed25519` and a public key named `qbic-upload.ed25519.pub` within your `.ssh` directory.

### Get in Contact

After you have [generated your ssh key](#generate-cryptographic-keys) and setup a public static IP address, 
please write an email to [support@qbic.zendesk.com](mailto:support@qbic.zendesk.com) and attach the public (.pub) key file similar to the provided template:

!!! warning 
    Make sure you **only** send us the public key file ending with .pub 

    **Do not send us the private key!**

```txt
Dear QBiC Team

I would like to upload measurement data to your data manager. 
Can you please provide me with an account on your upload server. 

Below you can find the requested information

Name: <Max Mustermann>
E-Mail: <max.mustermann@example.com>
Affiliation: <My Research Institute>, <https://ror.org/03a1kwz48>
Project: <Q2EXAMPLE>
Access Duration: 30 days

IP-Address: <Your static public IPV4 Adress>
For accessing your upload server I would like to use the attached key.

Attachments: qbic-upload.ed25519.pub
```

### Wait for a reply
After you have [established contact](#get-in-contact) with our support team, 
we will create an account for you on our upload server and contact you with confirmation and your assigned username.

!!! note 
    Please note down the username as this will be the username you will use to connect to our upload server.

### Proceed by [uploading data](raw_data_upload.md)
