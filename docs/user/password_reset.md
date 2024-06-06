# Password Reset

The data manager application provides an easy and secure solution 
to set a new password should a password associated with a user account be lost.
To reset your password the following steps have to be taken

1. Provide the account credentials for which the password should be reset
2. Follow the password reset link you received in your email 
3. Set a new password for the account according to the password policy

## Trigger Password Reset

From the login page you can navigate to a dedicated password reset site via the "Forgot password" link
on the bottom of the login
![login_password_reset](images/password_reset/password_reset.png)

You should now be able to see the password reset site:

![password_reset_email](images/password_reset/password_reset_email.png)

Please provide the email address of the account for which the password should be reset
and press the "Send" button which will send an email to the provided account with further instructions
![password_reset_email_sent](images/password_reset/password_reset_email_sent.png)

## Validate the Password Reset Trigger

Before the password of the provided account can be reset,
you need to validate that the account indeed belongs to you.
For this you will receive an email shortly after triggering the password reset, containing a unique password reset link
!!! warning "Spam Folder"
Please check your spam folder as well
Click the URL to follow the link, which will lead you to a page which allows you to set a new password for your account.
![validation page](images/password_reset/password_reset_new_password.png)

## Set a new password for the account

After your account has been validated, you can finally log in to the data manager. 
This can be done on the dedicated login page via the provided email address and password of the newly created account.
![login page](images/login_page_filled.png)
