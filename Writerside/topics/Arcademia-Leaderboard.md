# Arcademia Leaderboard

Arcademia Leaderboard is a hackable leaderboard service to allow our students to quickly and easily develop and deploy games with a shared leaderboard between all the arcade machines.

Arcademia (a play on the words 'arcade' and 'academia') is the name given to the arcade cabinets that have been converted from the Research Arcade project; these are now deployed to allow students to publish and share their games.

The system has been designed with the principal of 'habitability' in the terms of mod-ability and customisation from the students. We provide them full access to the source code - allowing them (if they choose) to open pull requests and issues, allowing for them to understand how the system actually works.

The arcademia project currently is not something that a student is required to take part in for the University degree.  

## Development

The arcademia leaderboard service is an express api, built with Josh's starter template. It is written in TypeScript and runs using Express and Node.

The development documentation is available in the repositories `README`, but a light overview is that;

- The project has been built in a devcontainer, which will automatically launch a `docker compose` file when you open the project in Visual Studio Code. This will provide you with an empty database which you will need to add an initial user account manually, and then create the games that you want to use for testing using an authenticated session state - this is best done using a tool such as [Postman](https://www.postman.com/), a collection has been provided in the repo. 

- And the system has been designed around the idea of 'Model-View-Controllers', however we are removing the 'View' aspect and are directly returning JSON from the controller. Each new controller must have a route, which is registered in the `src/server.ts` file.

## Deployment

Tbd....