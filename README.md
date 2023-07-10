# Monitoring
monitoring tools like Prometheus, Grafana, and collectd, as well as log management tools, enables proactive monitoring and troubleshooting.

This project uses Grafana, influxDb, collectd and prometheus mysql-exporter to monitor various metrics of a server.

Install grafana(ubuntu):

sudo apt-get install -y apt-transport-https

sudo apt-get install -y software-properties-common wget

wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add -

sudo add-apt-repository "deb https://packages.grafana.com/oss/deb stable main"

sudo apt install grafana

sudo /bin/systemctl daemon-reload

sudo /bin/systemctl enable grafana-server

sudo /bin/systemctl start grafana-server

sudo /bin/systemctl status grafana-server

Collectd Setup:

sudo apt-get -y install collectd

service collectd start

Installing InfluxDB

wget -qO- https://repos.influxdata.com/influxdb.key | sudo apt-key add -

source /etc/lsb-release

echo "deb https://repos.influxdata.com/${DISTRIB_ID,,} ${DISTRIB_CODENAME} stable" | sudo tee /etc/apt/sources.list.d/influxdb.list

sudo apt-get update && sudo apt-get install influxdb
sudo service influxdb start

influx
CREATE DATABASE collectd 
exit


