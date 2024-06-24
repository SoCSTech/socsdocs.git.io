# Traefik

[Traefik](https://traefik.io/traefik/) is a reverse proxy which runs on the [socs-web01](socs-web01.md) server. This provides ingress to all the web based containers.

This allows us to access the services we are running by using a hostname,  without having to remember an arbitrary port.

For example; you can access [asgard](Asgard.md) with the hostname `asgard.socstech.support`.

But be aware - this will only work if you're connected to the University network, as it is configured only to use a local IP.

> This isn't fully deployed yet and more documentation will be added at a later date.
{style="warning"}