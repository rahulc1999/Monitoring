# Monitoring
monitoring tools like Prometheus, Grafana, and collectd, as well as log management tools, enables proactive monitoring and troubleshooting.

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
