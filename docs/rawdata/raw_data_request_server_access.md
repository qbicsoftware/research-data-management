# Request server access

This page is for users outside the University of Tübingen network who need to upload data to the QBiC server.

!!! tip "University members"
    If you're at the University of Tübingen, you can [upload data directly](raw_data_upload.md) — skip this page.

## What you'll need

- An **ed25519 SSH key pair** on the machine you'll connect from
- The **public, static IPv4 address** of that machine
- Your **name and institutional affiliation**

## Generate an SSH key pair

SSH keys are a secure alternative to passwords for file transfers. Your computer generates two linked files: a private key (stays on your machine — never share it) and a public key (you send it to us). When you connect, the system checks that they match.

=== "Linux"

    ```bash
    ssh-keygen -t ed25519 -a 420 -f ~/.ssh/qbic-upload.ed25519 -C "<your_email@example.com>"
    ```

=== "macOS"

    Open Terminal ([how to](https://support.apple.com/guide/terminal/open-or-quit-terminal-apd5265185d-f365-44cb-8b09-71a064a42125/mac)):

    ```bash
    ssh-keygen -t ed25519 -a 420 -f ~/.ssh/qbic-upload.ed25519 -C "<your_email@example.com>"
    ```

=== "Windows"

    Open PowerShell ([how to](https://learn.microsoft.com/en-us/powershell/scripting/windows-powershell/starting-windows-powershell?view=powershell-7.5)):

    ```bash
    ssh-keygen -t ed25519 -a 420 -f $HOME/.ssh/qbic-upload.ed25519 -C "<your_email@example.com>"
    ```

This creates two files in your `.ssh` directory: `qbic-upload.ed25519` (private key) and `qbic-upload.ed25519.pub` (public key).

!!! danger "Never share your private key"
    Only send the `.pub` file. The private key file (without `.pub`) must stay on your computer.

## Request access

Send an email to [support@qbic.zendesk.com](mailto:support@qbic.zendesk.com) with the `.pub` file attached:

```text
Dear QBiC Team,

I would like to upload measurement data to the Data Manager.
Please provide me with an account on your upload server.

Name: <Your Name>
Email: <your.email@example.com>
Affiliation: <Your Institute>, <https://ror.org/your-ror-id>
Project: <Q2EXAMPLE>
Access Duration: 30 days

IP Address: <Your static public IPv4 address>

Attached: qbic-upload.ed25519.pub
```

!!! note "Static IP required"
    Check with your IT department about obtaining a public, static IP address for the machine you'll connect from.

## Wait for confirmation

The QBiC team will create your account and send you a username. Note it down — you'll need it to [connect and upload](raw_data_upload.md).

---

## What's next

➡ [Upload your data](raw_data_upload.md)
