
# WordPress with Docker Compose (Local Development)

## Prerequisites
- Docker Engine:`https://docs.docker.com/engine/install/`
- Docker Compose: `https://docs.docker.com/compose/install/`

## Installation

Clone the Repository

```bash
  [git clone https://github.com/<your-username>/<your-repository-name>.git](https://github.com/sourabh1234-sys/Docker-Wordprss.git)
```

Create the Volume (Optional)
```bash
  
  docker volume create wordpress-data
```
Start the Application
```bash
  docker-compose up -d
```

## Access WordPress

Open your web browser and navigate to http://localhost:5555/  (replace 5555 with the port you mapped for the web container if you changed it).

## Default Credentials
- Username: admin (you can change this in the environment section of web in docker-compose.yml)
- Password: 5566 (you can change this as well)

## Customization
- __Database Credentials__: Modify the MYSQL_ROOT_PASSWORD, MYSQL_USER, and MYSQL_PASSWORD environment variables in the db service of docker-compose.yml to suit your preferences.
- __WordPress URL__: Change the WORDPRESS_SITEURL environment variable in the web service of docker-compose.yml to define your desired WordPress site URL.
- __Ports__: Adjust the port mappings in the ports section of docker-compose.yml if you want to use different ports for accessing the WordPress instance.
- __Persistent Data__: If you created the wordpress-data volume, mount it to the /var/www/html directory in the web service of docker-compose.yml to persist your WordPress data.


```bash
  docker-compose exec web wp core update
```

## Contributing

We encourage contributions to improve this setup. Feel free to submit pull requests with enhancements or bug fixes.



## License

This project is licensed under the MIT License.

