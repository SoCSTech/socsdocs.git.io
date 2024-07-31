# Asgard

Asgard is the backend timetabling engine that provides content to [yggdrasil](Yggdrasil.md), 
it acts as a data aggregator and single point of truth to all display content.

More specifically we are using it to combine the data we get from multiple sources such as the UoL Timetable, Internet Calendars, Microsoft Bookings and Manually created events.

## Getting Started

You will need an account to use asgard, you should have been provided this during your onboarding.

![asgard-login.png](asgard-login.png)

When you have been given your account you will need to go through the password recovery process to set a password for your account.

The password for your account should be secure and not shared as if you have access to asgard you can put things on the signage screens, you should put this in your [1Password](1Password.md) employee vault.

You will need this password everytime you want to make a change to the signage.

You will either be given a 'technician' account or a 'standard' account. A 'technician' account has access to all timetables that exist inside the asgard system. 

## Day to Day

### Home

![asgard-home.png](asgard-home.png)

The asgard homepage is the page you will land onto first, it is a quick overview of the timetables that you're able to access (if you have a standard account) or the one's you've marked as favourite (if you have a technician account).

### Timetables

![asgard-timetables.png](asgard-timetables.png)

#### Add Timetable

![asgard-add-timetable.png](asgard-add-timetable.png)

#### Manage Timetable 

##### Events
![asgard-manage-timetable.png](asgard-manage-timetable.png)

##### Carousel
![asgard-carousel.png](asgard-carousel.png)

### Timetable Groups

![asgard-timetable-groups.png](asgard-timetable-groups.png)

## System Design
tbd...

## Development

tbd: discuss the other components and break down into subsections for api/y2/admin/etc.

The asgard api service is an express api, built with Josh's starter template. It is written in TypeScript and runs using Express and Node.

The development documentation is available in the repositories `README`, but a light overview is that;

- The project has been built in a devcontainer, which will automatically launch a `docker compose` file when you open the project in Visual Studio Code. This will provide you with an empty database which you will need to add an initial user account manually, and then create the games that you want to use for testing using an authenticated session state - this is best done using a tool such as [Postman](https://www.postman.com/), a collection has been provided in the repo.

- And the system has been designed around the idea of 'Model-View-Controllers', however we are removing the 'View' aspect and are directly returning JSON from the controller. Each new controller must have a route, which is registered in the `src/server.ts` file.


## Deployment

Tbd....