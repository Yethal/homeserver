## Homeserver

Compose file for my home server. Runs following services:
* Roon
* Plex
* Transmission
* Netboot.xyz
* Unifi Controller
* Nextcloud

Additionally, following auxiliary containers are included:
* Swag (combined Let's Encrypt client and Nginx reverse proxy)
* Dockerproxy (access limiter for Docker socket)
* MariaDB (database for Nextcloud)

### Deployment guide
1. Install docker and docker-ompose on your server
1. Clone this repository
1. Create a file named .env in the same directory as docker-compose.yml file
1. Add following environment variables to the files:
    * MYSQL_ROOT_PASSWORD
    * MYSQL_PASSWORD
    * MYSQL_DATABASE
    * MYSQL_USER
    * URL
    * EMAIL
    * DNSPLUGIN
1. Adjust volume mappings in the compose file to match your directory structure
1. Run `sudo docker-compose up -d`
