# Docker on seps-app01

We make extensive use of Docker on the Server and in the School too. Docker powers our sites, services and some of the 
student projects on this server! 

There will be a section added soon to discuss Docker a little more. 
We recommend you get yourself comfortable with the idea of using Docker before proceeding to make any changes to it on 
`seps-app01`.

## Gotchas!
* **You may find that after a reboot not all services are back up and running - these will need manually starting again!**
* If you notice a service that is consistently not restarted, raise an issue on the [GitHub Repo](https://github.com/SoCSTech/seps-app01).

## Using docker compose

We use docker-compose to start containers, rather than simply pulling and running containers directly.

To deploy a new service, clone the repo to your local machine, and create a folder named as the service and author a compose file describing your required deployment. 

## Monitoring Containers via `ctop`

<warning>
We are investigating replacing `ctop` as it is abandoned... This section will be updated in the future!
</warning>

As long as you have been added to the `docker` user-group, you will be able to use `ctop` to monitor, start, stop, restart
and view logs on a container. `ctop` offers a nice "UI" that you can use to check container statuses rather than relying
on `docker ps`.


