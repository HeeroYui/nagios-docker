nagios-docker
===========

Repository for wrapping `Nagios service` to be used together with `docker-compose`.

The default open port is 8080 and the basic user is ```nagiosadmin``` pass=```nagios```

License
=======

MPL-2

Clone the repository:
=====================

```
git clone https://github.com/HeeroYui/nagios-docker.git
cd nagios-docker
```

Compose and start your environement:
====================================

```
docker-compose up
```

If you prever do it in a deamon:

```
docker-compose -d up
```

Remove the current docker when started:

```
docker-compose rm mqtt
```


Create your password file, see documentation: ```https://mosquitto.org/man/mosquitto_passwd-1.html``` or update the file : ```config/passwd_readable```

and execute:
```
cd config
cp passwd_readable passwd
mosquitto_passwd -U passwd
cd ..
```

Common tools for docker:
========================


List all the active docker on the system
```
docker ps -a
```

remove a docker
```
docker rm NAME_OF_THE_CONTAINER
```

Start a docker compose with a clean interface
```
docker-compose up --force-recreate
```

