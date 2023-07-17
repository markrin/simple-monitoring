# simple-monitoring
test task implementing prometheus+grafana for simple web app


run commands: 
cd ./go-app
docker build --no-cache . -t go-app:0.x
docker run --rm -p 9000:9000 go-app:0.x

docker compose -d up

# for grafana connection use prometheus domain name: http://simple-monitoring-prometheus-1:9090