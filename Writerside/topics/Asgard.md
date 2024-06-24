# Asgard

Asgard is the backend timetabling engine that provides content to [yggdrasil](Yggdrasil.md), 
it acts as a data aggregator and single point of truth to all display content.

## Development

tbd: discuss the other components and break down into subsections for api/y2/admin/etc.

The asgard api service is an express api, built with Josh's starter template. It is written in TypeScript and runs using Express and Node.

The development documentation is available in the repositories `README`, but a light overview is that;

- The project has been built in a devcontainer, which will automatically launch a `docker compose` file when you open the project in Visual Studio Code. This will provide you with an empty database which you will need to add an initial user account manually, and then create the games that you want to use for testing using an authenticated session state - this is best done using a tool such as [Postman](https://www.postman.com/), a collection has been provided in the repo.

- And the system has been designed around the idea of 'Model-View-Controllers', however we are removing the 'View' aspect and are directly returning JSON from the controller. Each new controller must have a route, which is registered in the `src/server.ts` file.


## Deployment

Tbd....

## System Design
tbd...