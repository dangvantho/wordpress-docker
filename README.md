# docker-wordpress
A simplified yet refined Docker Compose workflow that sets up a LEMP network of containers for local WordPress development.
## Usage

To get started, make sure you have [Docker installed](https://docs.docker.com/docker-for-mac/install/) on your system, and then clone this repository.

Next, navigate in your terminal to the directory you cloned this, and spin up the containers for the web server by running `docker-compose up -d`.

After that completes, you make file php/wp-config.php from file php/wp-config-sample.php, adjust the following parameters:

```
/** Database name define in docker-compose.yaml */
define( 'DB_NAME', 'wp' );

/** Database username define in docker-compose.yaml */
define( 'DB_USER', 'wp' );

/** Database password define in docker-compose.yaml */
define( 'DB_PASSWORD', 'demo' );  

/** Database hostname */
define( 'DB_HOST', 'db hostname' );
```