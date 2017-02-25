A Prometheus blackbox_exporter Docker image for ARM architectures.  It ships with the blackbox_exporter.yml file
bundled with the official release, which will allow basic monitoring of HTTP, POP3, SSH, IRC, TCP, and ICMP endpoints.

To enable more deatailed monitoring, or configuring DNS probes, you'll need to setup a customized configuration
and mount it into the container.  Something like:

```
docker run -d -p 9115:9115 -v /local/path/to/blackbox_exporter.yml:/etc/blackbox_exporter/config.yml armhf-prometheus-blackbox_exporter:latest
```

See the official github repo: https://github.com/prometheus/blackbox_exporter for supported configuration settings.
