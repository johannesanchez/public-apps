# docker run -it -d --name prometheus -p 9090:9090 -v /var/www/html/docker/prometheus:/etc/prometheus prom/prometheus --config.file=/etc/prometheus/prometheus.yml 


*installing node_exporter in node Linux*
mkdir /node_exporter
cd /node_exporter/
wget https://github.com/prometheus/node_exporter/releases/download/v0.18.1/node_exporter-0.18.1.linux-amd64.tar.gz
tar -xvzf node_exporter-0.18.1.linux-amd64.tar.gz
cd node_exporter-0.18.1.linux-amd64/
./node_exporter &
netstat -plutona


*installing node_exporter in node Windows*
https://github.com/prometheus-community/windows_exporter/releases


## running grafana docker
docker volume create grafana-storage

#Run Grafana container with persistent storage (recommended)
docker run -d -p 3000:3000 --name grafana -v grafana-storage:/var/lib/grafana grafana/grafana

#docker run -it -d --name grafana -p 3000:3000 grafana/grafana


*after add a new target you have to restart or reload prometheus -- better pass the API Commnad to reload*


# docker restart prometheus

#some useful Grafana Dashboards
Grafana Windows Dashboard
10467 Windows Server
11515 Windows Server

!haj327#LASk4uP$