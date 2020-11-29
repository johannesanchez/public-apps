# docker search prometheus
# docker pull prom/prometheus 
# docker pull grafana/grafana
# touch touch /opt/docker/prometheus/prometheus.yml 
# /var/www/html/docker/prometheus
# docker run -it -d --name prometheus -p 9090:9090 -v /var/www/html/docker/prometheus:/etc/prometheus prom/prometheus --config.file=/etc/prometheus/prometheus.yml 


*installing node_exporter in node* 
mkdir /node_exporter
  225  cd /node_exporter/
  226  wget https://github.com/prometheus/node_exporter/releases/download/v0.18.1/node_exporter-0.18.1.linux-amd64.tar.gz
  228  tar -xvzf node_exporter-0.18.1.linux-amd64.tar.gz
  231  cd node_exporter-0.18.1.linux-amd64/
  233  ./node_exporter &
  234  netstat -plutona


## running grafana docker
docker volume create grafana-storage

#Run Grafana container with persistent storage (recommended)
docker run -d -p 3000:3000 --name grafana -v grafana-storage:/var/lib/grafana grafana/grafana


#docker run -it -d --name grafana -p 3000:3000 grafana/grafana

# docker ps -a
CONTAINER ID        IMAGE               COMMAND                  CREATED              STATUS              PORTS                    NAMES
26ea5cc6eae7        grafana/grafana     "/run.sh"                About a minute ago   Up About a minute   0.0.0.0:3000->3000/tcp   grafana
9e20836a2cb2        prom/prometheus     "/bin/prometheus --c…"   2 hours ago          Up 10 minutes       0.0.0.0:9090->9090/tcp   prometheus



For Windows:
https://github-production-release-asset-2e65be.s3.amazonaws.com/66566232/ce420180-ba90-11e9-835e-e3169fea1013?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAIWNJYAX4CSVEH53A%2F20200316%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20200316T102901Z&X-Amz-Expires=300&X-Amz-Signature=2a674340e84b18c0d422a2de91eafd4d919baa14cfd35d9ce58c9f288d57b203&X-Amz-SignedHeaders=host&actor_id=41158101&response-content-disposition=attachment%3B%20filename%3Dwmi_exporter-0.8.1-amd64.msi&response-content-type=application%2Foctet-stream


*after add a new target you have to restart or reload prometheus*
# docker restart prometheus

Grafana Windows Dashboard
1941 Windows Server
10467 Windows Server
