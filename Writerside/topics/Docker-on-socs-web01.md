# Docker on socs-web01

We make extensive use of Docker on the Server and in the School too. Docker powers our sites, services and some of the 
student projects on this server! 

There will be a section added soon to discuss Docker a little more. 
We recommend you get yourself comfortable with the idea of using Docker before proceeding to make any changes to it on 
`socs-web01`.

## Gotchas!
* **You may find that after a reboot not all services are back up and running - these will need manually starting again!**

## Using `docker-compose`

Please use docker-compose to start containers, rather than simply pulling and running containers directly. Store the
`docker-compose.yml` in a directory relating to that service you are trying to run. This allows for easier maintenance.

## Monitoring Containers via `ctop`

As long as you have been added to the `docker` user-group, you will be able to use `ctop` to monitor, start, stop, restart
and view logs on a container. `ctop` offers a nice "UI" that you can use to check container statuses rather than relying
on `docker ps`.


