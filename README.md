This project uses the following technology stack:

-   [Vue.js](https://vuejs.org/as) as a frontend framework,
-   [Laravel](https://laravel.com/) as a backend framework,
-   [MySQL](https://www.mysql.com/fr/) as a database management system.

To simplify our developement phase, we have used [Laravel Sail](https://laravel.com/docs/9.x/sail) which is a built-in solution for running our project using [Docker](https://www.docker.com/).

## Prerequisite

In order for your to run this project, you should have [Docker](https://www.docker.com/) installed on your computer.

## Installation

-   1. Clone the project by entering the command below in your
       prefered location:

```sh
git clone https://github.com/Toulix/food-zero.git && cd food-zero
```

-   2. Navigate to the application's directory folder and then type the following command to install the application's dependencies:

```sh
docker run --rm \
    -u "$(id -u):$(id -g)" \
    -v $(pwd):/var/www/html \
    -w /var/www/html \
    laravelsail/php81-composer:latest \
    composer install --ignore-platform-reqs
```

This command uses a small Docker container containing PHP and Composer to install the application's dependencies.

-   3. Start sail by executing the following command:

```sh
./vendor/bin/sail up
```

-   4. For the frontend part, open a new terminal and cd to the application's folder
       by typing:

```sh
npm install && npm run dev && php artisan migrate
```

-   5. Once the application's containers have been started, you may access the project in your web browser at: http://localhost.
