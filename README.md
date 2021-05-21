# docker-rails5

## Version 

Ruby : 2.6.5

Rails : 5.2

Postgres : 12.5

## Build (only for the first time)

### create rails application
~~~
docker-compose run --rm --no-deps rails rails new . --force --database=postgresql
~~~

### create database
~~~
cp -p local/rails/database.yml.org local/rails/config/database.yml
docker-compose up -d --build
docker exec local_rails rake db:create
~~~

## Access

(it'll take some time.)

access http://localhost:3000/


## Stop

~~~
docker-compose down
~~~

## Start

~~~
docker-compose up -d
~~~

## Create sample rails app

~~~
docker-compose up -d
docker exec local_rails rails generate scaffold user name:string age:integer area:string
docker exec local_rails rake db:migrate
~~~

access 
http://localhost:3000/users





