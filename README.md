# docker-rails

## Version 

Ruby : 2.6.5

Rails : 5.2

Postgres : 12.5

## Build

~~~
docker-compose run --no-deps rails rails new . --force --database=postgresql
sudo chown -R $USER:$USER .
cp -pi local/rails/database.yml.org local/rails/config/database.yml 
docker-compose up -d --build
~~~

## Start

~~~
docker-compose up -d
~~~

(it'll take some time.)

access http://localhost:3000/

## Stop

~~~
docker-compose down
~~~






