# Settings
- Copy this folder into of the your application
- Edit the file .env with your settings
- In the docker-compose.yml, where is "\<app-network\>", replace with name of the network app
- Also edit in the /nginx/conf.d/app.conf: 

    Search by "fastcgi_pass \<app\>:9000;" and where is \<app\> replace to your app name.

# Commands
Create and execute all images in the settings of the docker-compose
- docker-compose up -d

Create and execute selective images
- docker-compose up -d app webserver

Exec commands in container: docker-compose exec <name-container> <command>
- docker-compose exec app php artisan
- docker-compose exec app php -i
- docker-compose exec db mysql
- docker-compose exec app ls
