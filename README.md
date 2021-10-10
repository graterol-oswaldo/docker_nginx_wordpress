# Docker: Nginx, PHP and MySQL

Services container infrastructure integrated by NGINX, MySQL and PHP, designed to deploy WordPress websites.

## Description

This project it is integrated by:

- NGINX
- PHP
- MySQL

As a developer looking to improve my skils and abilities in the domain of Docker and WordPress CMS, I share this container structure in interest of making it easier to deploy both development and production environments.

## Getting Started

### Dependencies

Docker Compose relies on Docker Engine, so make sure you have Docker Engine installed. For more information related to the installation process, check the [official Docker page](https://docs.docker.com/compose/install/).

### How to use

1. Navigate to the main github page of the repository
2. Above the file list, click **Use this Template** to [create a new github repository from this template](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template#creating-a-repository-from-a-template)
3. Clone your new repository
4. Customize the names of your services, replacing the patterns "service-" and "\_service" by "app-name-" and "\_app_name" respectively, replacing the matches found in ./docker-compose.yml and ./php/app.conf files.
5. From your local copy and under root directory:
   1. Create an .env file from .env.example file and set the environment varibles.
   2. Run `docker-compose up -d --build`
6. Download and extract WordPress. Under `src` directory:
   1. Run `wget https://wordpress.org/latest.tar.gz`
   2. Run `tar -xzvf latest.tar.gz`
   3. Run `rm latest.tar.gz`
7. Setup WordPress from `wp-config.php`. Under `src/wordpress` directory:

   1. Run `wp-config-sample.php wp-config.php`
   2. From the variables set in the `.env` file, replace or complete the section in the `wp-config.php` file with your corresponding values:
   <pre><code>
   // ** MySQL settings - You can get this info from your web host ** //
   /** The name of the database for WordPress */
   define( 'DB_NAME', 'database_name_here' );

   /\*_ MySQL database username _/
   define( 'DB_USER', 'username_here' );

   /\*_ MySQL database password _/
   define( 'DB_PASSWORD', 'password_here' );

   /\*_ MySQL hostname _/
   define( 'DB_HOST', 'localhost' );
   </code></pre>

   3. Complete WordPress install process, from URL: 0.0.0.0:8000.

<!--
 ### Executing program

 * How to run the program
 * Step-by-step bullets
 ```
 code blocks for commands
 ```

 ## Help

 Any advise for common problems or issues.
 ```
 command to run if program contains helper info
 ```

 ## Authors

 Contributors names and contact info

 ex. Dominique Pizzie
 ex. [@DomPizzie](https://twitter.com/dompizzie)
-->

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
