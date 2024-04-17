# Windows Settings

## User Accounts

2 user accounts are required for the lab image, the standard 'Computing' account used by students, and a SoCSTech Admin Account accessible only to us.

| Username       | Password                        |
|----------------|---------------------------------|
| Computing      | computing                       |
| SoCSTech Admin | Check Current Password Rotation |

## GPO

Group policy is not something widely used on the image at the moment, but this is something that will be written up in more detail once the next image is created.

## AUP Message

An Acceptable Usage Policy message should be displayed as the user logs in to the computing account, displaying the lab 
rules. This is set up by opening 'Edit group policy' and navigating to 'Computer Configuration\Windows Settings\Security 
Settings\Local Policies\Security Options\Interactive Logon: Message text for users attempting to log on'. The message title
also needs to be configured at the 'Interactive Logon: Message text for users attempting to log on setting'.

A text file displaying the AUP message may be stored in the PubMedia folder in case it needs to be accessed again, but this is optional.