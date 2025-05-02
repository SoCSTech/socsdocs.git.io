# Policies

On DeepFreeze we have a couple of policies that we use that change the characteristics of how the lab PCs work.

> When moving machines between policies and groups, you should check that all the machines have been refrozen before you reopen the space.
{style="warning"}

## Computing Policy

This is the default policy, this is for student facing machines where they should reboot after a period of time and also have some restrictions in place.

## Events Policy

This is the opposite of the computing policy. We use this for events such as Game Jams, Hackathons and _some_ Exams. The computers are unrestricted and will not reboot after a period of time. 

This is useful as it allows for lab users when they are at a game jam, and force them to have a shower, eat, or just generally move around!

When moving between Events and Computing you should check the power saving icon is green to indicate that it is installed and not just 

![df-power-saving](df-power-saving.png)

## Exam Policy

We have a policy we use for Blackboard exams. This configures the machine to use WINSelect which restricts the machine into only using the Blackboard site.

## Splashtop Policy

This is for our [Splashtop machines](Splashtop.md), this policy enforces the controls we discuss in the Splashtop section.

This should largely be similar to the Computing Policy.

## Your Testing

It is highly encouraged that you create a testing policy that you can deploy and destroy! This is useful figuring our what quirks are with Deep Freeze, but without affecting the labs too much - as you can work by only taking a limited amount of machines out of action.

## Server Policy

This is used for Windows machines which are used as servers, this is useful so we can keep a track of stuff such as IP addresses and have some level of control of Windows Updates.