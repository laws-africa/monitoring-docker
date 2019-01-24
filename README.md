# Monitoring docker configuration for hosts

This installs common monitoring on our hosts.

* Metricbeat: monitors system and docker usage

# Installation

Install [docker-compose](https://linuxize.com/post/how-to-install-and-use-docker-compose-on-ubuntu-18-04/):

1. `sudo curl -L "https://github.com/docker/compose/releases/download/1.23.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose`
2. `sudo chmod +x /usr/local/bin/docker-compose`

Install this package:

1. `git clone https://github.com/laws-africa/monitoring-docker.git`
2. `cd monitoring-docker`
3. `sudo setfacl -m u:1000:rw /var/run/docker.sock`
4. `echo "HOSTNAME=${HOSTNAME}" >> .env`
5. `docker-compose up -d`
