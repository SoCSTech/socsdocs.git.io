# Setting Up

## TL;DR

- Login with shared account
- Download apps as required
- Delete user projects
- Enable dev mode
- Reset zones

## User Account

We have a shared account for the quest headsets, we use this because this allows us to not enforce students to log in with their own accounts which causes two problems, one compliance and one logistical. What if a student does not want to use Meta services? If we let students login with their own account, how do we remove this from the headsets once they're done?

So to combat this we log in with a generic `SoCS Technician` account; for all intents, this is an empty account that we control. The account password and 2FA codes are in [1Password](1Password.md).

## Downloading Software
The lecturers for VR should let you know what software is required to be on the headsets.

Most typically, they will need nothing to be preinstalled unless they're using the headsets to demonstrate something or using it for an [Offer Holder/Open Day](Offer-Holder-Open-Days.md), and then they will let you know beforehand.

## After Use
You should remove all student data from the headsets once they have been used. This can be as simple as removing apps that have been installed by the students (this could be their assignments!) or fully resetting the headset.

The headsets should be reset regularly to ensure that random files such as caches are removed.

## Developer Options

We do not have our headsets centrally managed to ensure that students can develop on the headsets, which requires the students to install random, unsigned apks - they have made these!

We need to allow the following settings to allow them to do that:

- Become developer (typically done by hitting the build number ~10 times - it will then say 'You are now a developer')
- Allow Unsigned Apps
- Allow USB Debugging

The location of these settings change semi-frequently, but they are in <kbd>Settings</kbd> > <kbd>Developer</kbd>.


