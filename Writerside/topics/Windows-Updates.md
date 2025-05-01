# Windows Updates

When first creating a fresh image, the first and last thing you should do is check for and install Windows Updates, until it displays the following 'You're up to date' message.

![WindowsUpdated](WindowsUpdated.png)

Once Windows is up to date, you should then pause updates for 5 weeks. This is to prevent a rogue Windows Update breaking a piece of software or some other configuration.


## Holding Major Changes

You should then edit the group policy to stay on a specific version of Windows, we want to do this for the whole academic year to ensure software has been tested appropriately.

Before you start you should have made sure that you have the most up-to-date version of Windows.

First, run `winver` to find out which version you have installed - this should be something like `24H2` we will be using this for our example. 

Then open `gpedit` (group policy editor), and update the following object:

```
Computer Configuration > Administrative Templates > Windows Components > Windows Update > Manage updates offered from Windows Update
```

Ensure that you have ticked enabled, and set the `Windows product version` to `Windows 11` and the feature updates target version to be `24H2`.

![image_83.png](image_83.png)