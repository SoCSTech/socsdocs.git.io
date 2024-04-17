# Splashtop

Splashtop is the service we use for remote access to lab machines. Currently, we have a suite of machines dedicated
to run Splashtop at the front of Labs 1A and 2B (hopefully this changes in the future).

## Installing Splashtop
Splashtop is installed with an installer which can be provided by the technical resource manager. It should be
installed just prior to DeepFreeze.

## Splashtop Configuration
Splashtop machines are set up as either Windows or Ubuntu, so the boot order needs to be changed and GRUB needs
to be disabled to ensure that the machine directly boots into the desired OS.

The machine also needs to be put into the Splashtop group on DeepFreeze, which has an enforced Splashtop
policy. This policy forces the machines to restart after being idle for a pre-defined amount of time. This is useful
to make sure that people aren't AFK to reserve Splashtop machines.