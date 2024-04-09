# DeepFreeze

DeepFreeze is one of the most critical tools we have in our arsenal.

It has been implemented in our labs to offer a reboot-to-restore functionality to all our student facing machines. That means that everytime a PC is reboot, a clean snapshot is applied to the machine.

A byproduct of using this solution is that we also gain a degree of remote management on our lab PCs.

This topic will have multiple subtopics added which discuss the remote services that we use in our day to day, and how to deploy it effectively.

## Why we use it
Many a technician ago, the School began to have some issues with its open-access labs. You will have noticed that (at the time of writing) we have a single login for all students with an easy password.

This is great as it means everything we do as school that could potentially break a corporate setup, will only really affect a single machine - and this gives us a greater degree of flexibility for running our modules.

However, issues with plagiarism, compromised and stolen accounts, and, illicit materials started to appear. DeepFreeze negates this, as every time a machine is restarted, it reverts to a clean state. DeepFreeze will automatically restart a machine to apply this on log out, or, whenever a idle timer is hit.
