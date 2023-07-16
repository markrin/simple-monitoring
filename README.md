# simple-monitoring
test task implementing prometheus+grafana for simple web app


run commands: 
cd ./go-app
docker build --no-cache . -t go-app:0.4
docker run --rm -p 9000:9000 go-app:0.4

