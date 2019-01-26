testdriven-app

Docker configL

Step
$ docker-machine env testdriven-dev

execute as:
$ sudo docker-machine env testdriven-dev

Error:
'$ eval' doesnt work immidiatly
first:
$sudo chown -R mickvermaat ~/.docker

Error2:
' Error checking TLS connection: machine does not exist'
Try: $ docker-machine restart default


issue:could not find flask-sqlalchemy even when specified in docker requirements.txt
temp fix: solved by opening the env (source services/users/env/bin/activate)
then install flask-sqlalchemy through pip

issue:
Micks-MacBook-Pro:testdriven-app mickvermaat$ docker exec -ti $(docker ps -awf "name=users-db") psql -U postgres
See 'docker ps --help'.
Error: No such container: psql
Fix: typo: -awf must be -aqf

Error: No such command "recreate_db".
typo: must be 'recreate-db' with dash instead of underscore
edit: its not a type. Somehow the source code def name with an _ underscore will only be callable from the cli terminal with a - dash.

Continue: Trying to run create testdiven-prod, but getting an authentication error

Create an AWS EC2 nano instance in FRankfurt:
$ docker-machine create --driver amazonec2 --amazonec2-region eu-central-1 --amazonec2-open-port 5000 testdriven-prod 


Switch between virtual envs in docker:
create docker-machine env:
$ docker-machine create --driver virtualbox  testdriven-dev

set environment
$ docker-machine env testdriven-dev
or

eval env
$ eval $(docker-machine env testdriven-dev)
or
eval $(docker-machine env testdriven-prod)


in .yml folder:
$ docker-compose -f docker-compose-dev.yml build
or
$ docker-compose -f docker-compose-prod.yml build

launch virtualbox:
$ docker-compose -f docker-compose-dev.yml up -d
or
$ docker-compose -f docker-compose-prod.yml up -d

recreate db
$ docker-compose -f docker-compose-dev.yml run users python manage.py recreate_db
or
docker-compose -f docker-compose-prod.yml run users python manage.py recreate_db

seed db
$ docker-compose -f docker-compose-dev.yml run users python manage.py seed-db

$ docker-machine ip testdriven-prod

docker instance should now be online accessable

if DM says docker mac app is not open:
$ eval $(docker-machine env testdriven-prod)
then
$ docker-machine regenerate-certs testdriven-prod



test app:
$ docker-compose -f docker-compose-prod.yml run users python manage.py test

