# Monitoring docker configuration for hosts

This installs common monitoring on our hosts.

* Metricbeat: monitors system and docker usage

# Installation

1. Clone this repo
2. `cd monitoring-docker`
2. `sudo setfacl -m u:1000:rw /var/run/docker.sock`
3. Set `HOSTNAME=the-host-name` in `.env`
3. `docker-compose up -d`
