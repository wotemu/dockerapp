# README

Learn how to use docker / docker compose to create and run rails application.

## Tested on

* Mac OSX - 10.10.5
* Docker - 1.12.1
* Docker compose - 1.8.0

## Instructions / commands

```
mkdir ~/projects/noteapp
cd ~/projects/noteapp
# Create Gemfile
# Create Dockerfile
# Create docker-compose.yml
docker-compose run app rails new . --force --database=mysql --skip-bundle
docker-compose build
docker-compose up
# http://localhost:3001
docker-compose run --rm app rails g scaffold note title body:text
docker-compose run --rm app rake db:migrate
# http://localhost:3001/notes
#
```