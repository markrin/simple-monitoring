# simple-monitoring
test task implementing prometheus+grafana for simple web app


run commands

for web app itself:
> cd ./go-app

> docker build --no-cache . -t go-app:0.x

> docker run --rm -p 9000:9000 go-app:0.x

for full setup:
> docker compose -d up

go to browser and open Grafana UI
http://localhost/3000

log in with creadentials log/pass admin1/admin1

click Dashboards > my dashboard

------
!!! take a look at 'Helm' branch please