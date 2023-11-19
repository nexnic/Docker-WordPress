# Wordpress with MariaDB
This will be used for setting up local test environments,
Using WordPress API, it easy to set en maintain by the Developer, MariaDB image, and WordPress Image

## Built With
Here, You will find the tech used to build this Development. environment 

- [Docker](https://www.docker.com/)
- [Mariadb](https://hub.docker.com/_/mariadb)
- [Wordpress](https://hub.docker.com/_/wordpress)

### Version
    
    **Docker**
        Test On
        **Docker Desktop**
            V4.25.1
        **Docker Engine**
            V24.0.6
        **Docker API**
            V1.43
    **MariaDB**
        Test On
        **Mariadb Image**
            V10.6.4-focal
    **Wordpress**
        Test On
        **Wordpress Image**
            V6.3

## Getting started

Before using this docker container, install Docker Desktop or Docker engine [Link]().

When you have completed the install of Docker Desktop or Docker Engine
need to download this Repository. 

When you have completed download this Repository let's start building this 

Open the terminal and type in

```
    $docker compose up -d

    [+] Running 33/2
    ✔ db 10 layers [⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿] 0B/0B Pulled  
    ✔ wordpress 21 layers [⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿] 0B/0B Pulled
    [+] Building 0.0s (0/0)
    [+] Running 5/5
    ✔ Network docker-wordpress_default        Created
    ✔ Volume "docker-wordpress_wp_data"       Created
    ✔ Volume "docker-wordpress_db_data"       Created
    ✔ Container docker-wordpress-db-1         Started
    ✔ Container docker-wordpress-wordpress-1  Started

```

Now let's check if Container is running 

```
    $docker ps

    CONTAINER ID  IMAGE                COMMAND                CREATED       STATUS       PORTS               NAMES
    1692887413d4  wordpress:latest     "docker-entrypoint.s…" 4 minutes ago Up 4 minutes 0.0.0.0:80->80/tcp  docker-wordpress-wordpress-1
    095176d0a792  mariadb:10.6.4-focal "docker-entrypoint.s…" 4 minutes ago Up 4 minutes 3306/tcp, 33060/tcp docker-wordpress-db-1
```

Stopping and removing the Docker Container 

```
    $docker compose down
```

To remove alle the data on 

```
    $docker compose down -v 
```
