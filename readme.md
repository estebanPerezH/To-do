Development Environment
This project runs on a LEMP stack (Linux, NGINX, MySQL, & PHP).



The backend built with Laravel. The frontend is 100% React.




If you don't already have a LEMP environment running, Valet is a good option for OSX.




Set Up
Clone the repository:
Create your environment file:
cp .env.example .env
The app key is used to salt passwords. If you need to work with production data you'll want to use the same app key as defined in the .env file in production so password hashes match.




Update these settings in the .env file:
DB_DATABASE (your local database, i.e. "todo")
DB_USERNAME (your local db username, i.e. "root")
DB_PASSWORD (your local db password, i.e. "")
HASHIDS_SALT (use the app key or match the variable used in production)
Install PHP dependencies:
composer install
If you don't have Composer installed, instructions here.




Generate an app key:
php artisan key:generate
Generate JWT keys for the .env file:
php artisan jwt:secret
Run the database migrations:
php artisan migrate
Install Javascript dependencies:
npm install
If you don't have Node and NPM installed, instructions here.





Run an initial build:
npm run development
Additional Set Up Tips
Database Seeding
If you need sample data to work with, you can seed the database:

php artisan migrate:refresh --seed --force

 
