# Yggdrasil

Yggdrasil is the frontend timetable component for the signage screens around the building. It collects its data from [asgard](Asgard.md) and displays the data in the most effective way.

## Development

First, you'll need to clone the repo [SoCSTech/yggdrasil-revamp](https://github.com/SoCSTech/yggdrasil-revamp).

Then you will need to have either **Node 14** installed on your machine (I recommend that you use [nvm](https://github.com/nvm-sh/nvm) for this as we use multiple versions in our day-to-day operations.)

Once you have `nvm` installed, you can install Node 14 with the following commands;

```Shell
nvm install 14
nvm use 14
```

Then you will want to launch the live server with the command:
```Shell
npm run dev
```
This will allow you to make changes to the project and see the changes happen as you save.

Once you have done making your changes - you will need to commit these changes back to the repo (in your own branch), which will then allow for the project to be signed off and deployed.

### Apple Silicon
If you're using an ARM based CPU (e.g. Apple Silicon) this won't work without additional steps, as this project is running with node 14 (very old - end of life), and hasn't be upgraded (yet?).

You will need to first install and use [nvm](https://formulae.brew.sh/formula/nvm#default), I recommend you do this with [HomeBrew](https://brew.sh).

Then you need to run the following command to allow your terminal to run in Rosetta mode (64 bit compatibility mode):

```Shell
arch -x86_64 zsh
```

Then you can run the commands to use and install node 14.

## Deployment

tbd...