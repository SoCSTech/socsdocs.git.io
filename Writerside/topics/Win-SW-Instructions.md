# Windows Software Instructions

Most software can be installed normally, but the software which needs to be set up and configured in a particular way is detailed in this page.

## Houdini
Instructions for installing Houdini can be found on their website. Houdini needs to be licensed from the alic04.network.uni license server. This is easy enough to figure out by running the Houdini license administrator application. 

## Unity
Unity needs to be licensed with a script which runs upon startup. This script can be found in the NAS under Installers, but it needs to be updated every academic year  with a new license code and directory to unity installation.

```
@echo off
cd "C:\Program Files\Unity\Hub\Editor\2022.3.33f1\Editor"
Unity.exe -batchmode -username technician@lincoln.ac.uk -password Socks2021 -serial E4-3FYC-PKAQ-747G-93WB-UKVG -quit
```
Put a shortcut to this script into shell:startup and change the properties of the shortcut to make it run minimised.


## EG Launcher and Unreal Engine

The Epic Games launcher needs to be signed in using the account details on 1Password.

## Oculus Dev App

The Oculus Dev App needs to be signed in using the Meta account on 1Password.

## Docker

### Module Docker Containers

Many modules are containerised with the images hosted on GitHub. The repos for all of these modules are cloned to the master with a script that automatically pulls all repos upon boot. This script can be found on the NAS under Installers.

### PHPMyAdmin and MySQL
These docker containers need to run for multiple modules. We use the latest phpmyadmin docker image, and mysql:8-oracle.

After you have pulled these images, the following docker commands should be run to configure the containers correctly.

``docker pull mysql:8-oracle``

``docker pull phpmyadmin:latest``

``docker network create mysqlnetwork``

``docker run --name=MySQL --network=mysqlnetwork --env=MYSQL_ROOT_PASSWORD=computing --env=PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
--env=MYSQL_VERSION=8.4.2-1.el9 --env=MYSQL_SHELL_VERSION=8.4.1-1.el9 -p 3306:3306  -d mysql:8-oracle``

``docker run -d --name=PHPMyAdmin --network=mysqlnetwork --env=UPLOAD_LIMIT=300M --env=PMA_HOST=MySQL --env=PMA_PORT=3306 -p 9999:80 phpmyadmin:latest``

You can now visit localhost:9999 in a web browser to access the PHPMyAdmin panel to verify it worked. The username 'root' and password 'computing' should log you in.

### PGAdmin and PostgreSQL
These docker containers need to run for Scalable Database Systems. It has been set up for AY2425 like this:

```docker pull postgres:16```

```docker pull dpage/pgadmin4```

```docker network create postgresnetwork```

```docker run -d --name PostgreSQL --network postgresnetwork -e POSTGRES_PASSWORD=computing -e POSTGRES_USER=ROOT -p 5432:5432 postgres:16```

```docker run -d --name PGAdmin --network postgresnetwork -e PGADMIN_DEFAULT_EMAIL = student@lincoln.ac.uk -e PGADMIN_DEFAULT_PASSWORD=computing -p 9998:80 dpage/pgadmin4```

You can now visit localhost:9998 to access the PGAdmin panel to verify it worked. The email is student@lincoln.ac.uk and the password is 'computing'.