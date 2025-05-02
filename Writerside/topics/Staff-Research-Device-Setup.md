# Staff/Research Device Setup

This is a real big case of it depends. Try and get an idea of what they want beforehand.

## Corporate Machine

If an academic is wanting a standard/corporate machine, refer them to DT who will pick it up and deploy it, we should not really have involvement in this.

## Old Lab PCs

Sometimes, academics want a device that is specifically how they like it (but doesn't really care what specs their PC has), then there is two options on how to request the PC, either you need to talk to DT and ask them to deploy it, or you the technician can deploy it.

If it is being deployed by technicians, you need to ask the PI/Supervisor to submit a ticket to DT to receive authorization.

Here is a template email that you could modify and send to them, obviously confirming if you have stock first.

If you run out of stock, contact DT who will arrange for a small quantity to be left in our control.

```
Hi DT

Please could my PGR/Employee/Lecturer (Name) be provided with one of the former Computer Science lab PC's. The school technicians have advised they are able to fulfil the request from stock they have available, but the following information needs confirming first. (Name of Technician) will follow up with an asset number and disk wipe certificate for the DT asset list.

College:
School:
Programme (MSc, PhD, PGT course name):
Programme lead/PI or supervisor (academic):
Internal/External funds available:
Project/research name:
Length of project/research:
What data is collected on the requested device (data compliance - what is the data, anything personally identifiable?):
How many devices required: 1 (PC)
How many users will utilise it: 1 (User name)
Where the device is going to physically installed: INB....
Device use case (general use, not specification e.g. high performance, gaming, machine learning, etc):

Best,
(Name)
```

Once this has been accepted by DT, someone from service desk will contact you to let you know it can get sorted.

First, download [ShredOS](https://github.com/PartialVolume/shredos.x86_64) to a USB memory stick and then run it on the PC, you should ensure that you collect a destruction certificate once this has been run.

> We have found that running this on a Ventoy USB Stick does not work as expected.

Save the certificate to the USB stick and then power off the machine, upload this to our [Snipe-IT](Snipe-IT.md) as a file attachment to the asset, this keeps it inside the technicians team for our records.

Then send an email/teams message back to DT with the ticket details (or other reference they've provided) giving them the destruction certificate and the serial number, asset tag and MAC address of the pc. They will then check it out on their end and ensure they've kept the records that they want.

Then you can return back to setting up the PC.

Now you should check to see what the IP address of the PC is getting, we need to ensure for safety and security reasons that it is not in the `Computing Labs Vlan/Group`, also if it is connected to the wrong comms room (aka not <tooltip term="inb-phase2">INB Phase 2</tooltip>) it will not authenticate.

You need to check that the IP you get on the university network is NOT in the v4 subnet of 10.5.24.0/24. (That's anything from 10.5.24.0 to 10.5.25.255)

If it is in that subnet, raise another ticket with DT (this will be forwarded to the networks team, hence why you need to open another ticket) asking for them to remove that PCs MAC Address from the SoCS Lab Vlan, and they will make sure it works.

Then you should offer install and encrypt whatever OS and software they want. They may want to do this themselves and DT is happy for this to happen.

### Special

This should be done on a case by case basis, but the academic should always be referred to DT as this is out of our hands. DT may ask that we help with the management of the PC once it has been deployed or setting it up for them but this is uncommon.