# Custom Applications

This section is about deploying packages for Deep Freeze to roll out to the labs. This is useful for software that is regularly updated. This allows for the raw lab image to be as light as possible.

## Check with Faronics

If there is a popular piece of FOSS/Freeware Software, Faronics might have already added this as a piece of software that they will manage.

You should check this by going to `Polices` (on the nav bar) and then select your policy, and then `Software Updater`, `Applications`.

![df_policy_softupdater.png](df_policy_softupdater.png)

If the piece of software you want installing is not supported by Faronics, check with them to see if this is something they would support. You contact a deployment specialist by going to `Applications`, `Custom App`, `Create a Custom App`, and then `Talk to a Deployment Specialist`.

If they agree to support it, you can just apply the application to the policy.

## Setup a Custom App

First check the app does not already exist - even if that version is out of date.

Then open `Applications` > `Custom App` > `Create a Custom App`.

Then provide details such as the package name, if you need to restart the pc after installing, how long the installation should take before timing out, and how should it be installed (system account, normally a good choice!).

You should then find the URL of the installer, if you can - use a MSI as these are designed for scripted deployments (either through Deep Freeze like what we do, or SCCM, InTune or GPO like DT do!)

![df_app_window.png](df_app_window.png)

If you are installing a `.exe` you will need to check what CLI options you will need to provide, you should figure this out by either reading the documentation for the app you're installing - or trial and error.

If you are using trial and error, a good one to try is `/S` as this is a standard option for a **S**ilent install.

![df_weka_app.png](df_weka_app.png)

After you have saved, you will need to validate the installation works.

## Updating your custom app

To update your app, it is pretty easy - you just need to update the URL of the installer. You can do this by going to: `Applications` > `Custom App` > `View Custom Apps` > `(the app you're updating)` > `Edit`.

After you have saved, you will need to validate the installation works.

You will then need to push maintenance out to the Lab PCs to install this. 

If it doesn't automatically upgrade you may have to edit the policy to remove the app, then run maintenance, then check that the app has been uninstalled, and then re-add it to the policy, then run maintenance, hope, and then its upgraded.

## Validating Installation

You will be asked to validate the installation. It helps if this is during term-time as the PCs will be already on and reporting in. If it is not - don't worry, turn some PCs on and give it 30 mins or so.

Make your changed actions as above, either updating or creating, and look for the orange warning triangle.

![df_gh_needs_validating.png](df_gh_needs_validating.png)

Then click `here` to open the new modal page.

![df_gh_verify_click_here.png](df_gh_verify_click_here.png)

Look at what PCs are available and pick one and then close the window. It helps if you can go to that PC physically.

![df_pcs_avail_app_upgrade.png](df_pcs_avail_app_upgrade.png)

Go back to the `computers` tab and find it, reboot it as thawed (under deep freeze) and enable maintenance mode for anti-executable. Wait for the machine to update and stay on this page until it says it is online and thawed.

Recomplete the above steps to get back to the list of machines that can be used to verify installation.

![df_select_pc_to_verify.png](df_select_pc_to_verify.png)

Select the PC and click next.

![df_app_verify_press_install.png](df_app_verify_press_install.png)

Wait for it to download and install.

![df_app_fail.png](df_app_fail.png)

Ensure the installation does not fail - if it does, go back and verify your settings.

Once it has passed verification stage, you can go back and push that out as a policy update.

Again, If at anypoint you need help you can contact a deployment specialist by going to `Applications`, `Custom App`, `Create a Custom App`, and then `Talk to a Deployment Specialist`.

