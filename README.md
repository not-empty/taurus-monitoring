# Taurus Monitoring

[![Latest Version](https://img.shields.io/github/v/release/kiwfy/taurus-monitoring.svg?style=flat-square)](https://github.com/kiwfy/taurus-monitoring/releases)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)

Project to monitoring all taurus queus using grafana and prometheus.

### Run

Requires [Docker](https://www.docker.com/get-started) and [Docker Compose](https://docs.docker.com/compose/install/) tool.

```sh
docker-compose up
```

### Grafana

[Grafana](https://grafana.com/) is expose on port `3000` and you can access your [dashboard](http://localhost:3000/)

### Prometheus

[Prometheus](https://prometheus.io/) is expose on port `9090` and you can access [all metrics](http://localhost:9090/)

### Agent

The agent used for this project is [Bull Exporter](https://github.com/UpHabit/bull_exporter). That project is an official export shared in [Bull project](https://github.com/OptimalBits/bull).

### Grafana Config

For config in Grafana like allow embedding graph or other config you can access and update [grafana.ini](https://github.com/kiwfy/taurus-monitoring/blob/master/grafana/grafana.ini).

For fixed or updates taurus metrics you can change the [dashboard.json](https://github.com/kiwfy/taurus-monitoring/blob/master/grafana/dashboards/dashboard.json).

For update or input another datasource type you can configure in [datasource.yaml](https://github.com/kiwfy/taurus-monitoring/blob/master/grafana/provisioning/datasources/datasource.yaml)

**For new dashboards you can just create another json in [dashboard](https://github.com/kiwfy/taurus-monitoring/tree/master/grafana/dashboards) folder**

### Production

For production it's necessary configure the environment `EXPORTER_REDIS_URL` with redis url connection. Ex: redis://localhost:6379/0

### Development

Want to contribute? Great!

The project using a simple config code.
Make a change in your file and be careful with your updates!

**Kiwfy - Open your code, open your mind!**
