<img src=".github/kpe_banner.png" />

<h1 align="center">Kibana Prometheus Exporter</h1>

<p align="center">
  <a href="https://github.com/qualifio/kibana-prometheus-exporter/actions/workflows/codeql-analysis.yml">
    <img src="https://github.com/qualifio/kibana-prometheus-exporter/actions/workflows/codeql-analysis.yml/badge.svg" alt="CodeQL Repo Badge" />
  </a>
  <a href="https://github.com/qualifio/kibana-prometheus-exporter/actions/workflows/release-wiki.yml">
    <img src="https://github.com/qualifio/kibana-prometheus-exporter/actions/workflows/release-wiki.yml/badge.svg?branch=main" alt="Release Wiki" />
  </a>
  <a href="https://snyk.io/test/github/qualifio/kibana-prometheus-exporter">
    <img src="https://img.shields.io/badge/Snyk-Secured-8A2BE2.svg?logo=snyk">
  </a>
</p>

> This project is a fork of https://github.com/pjhampton/kibana-prometheus-exporter.

<img src="https://raw.githubusercontent.com/qualifio/kibana-prometheus-exporter/master/.github/kibana_prometheus.png" alt="kibana prometheus exporter">

<p align="center">Once Installed, please visit http://localhost:5601/_prometheus/metrics</p>

- [Installing](#installing)
- [Docker](#docker)
- [Prometheus Config](#prometheus-config)
- [Metrics](#metrics)
- [Releases](#releases)

## Installing

First, locate the version you require on the [release page](https://github.com/qualifio/kibana-prometheus-exporter/releases). There is a couple of ways to install this plugin. The more common approach would be to download the correct version and run:

```
bin/kibana-plugin install https://github.com/qualifio/kibana-prometheus-exporter/releases/download/8.12.0/kibana-prometheus-exporter-8.12.0.zip
```

**Important**: Please don't build off and install from the trunk (master). This is a development / experimental branch so don't be that girl/them/guy, please. The `RELEASE/{NUM}` branches are the release branches. This process is shaped by the Kibana release process.

## Docker

You can install into your container with the following command (replace, or env set `${KIBANA_VERSION}`):

```
RUN bin/kibana-plugin install https://github.com/qualifio/kibana-prometheus-exporter/releases/download/${KIBANA_VERSION}/kibana-prometheus-exporter-${KIBANA_VERSION}.zip
```

## Prometheus Config

Below is an example prometheus config.

```
- job_name: 'kibana'
  scrape_interval: '10s'
  metrics_path: '_prometheus/metrics'
  static_configs:
  - targets: ['localhost:5601']
  basic_auth:
    username: 'elastic'
    password: 'changeme'
```

## Metrics

Details on the various exported metrics are documented on the [Github wiki page](https://github.com/qualifio/kibana-prometheus-exporter/wiki).

## Releases

*The version of this plugin must match the version of Kibana you are running.* [Click here](https://github.com/qualifio/kibana-prometheus-exporter/releases) to download the available versions. If you don't see the version you want, please feel free to open an issue to request.

| Release | MD5 / SHA1 / SHA256 / SHA512   | Release Artifact - This must match your Kibana version |
|---------|-------------------------------|------------------------------------------------------------------|
| 8.16.1 | [checksum.json](https://github.com/qualifio/kibana-prometheus-exporter/releases/download/8.16.1/checksum.json) | [kibana-prometheus-exporter-8.16.1](https://github.com/qualifio/kibana-prometheus-exporter/releases/tag/8.16.1) |
| 8.15.3 | [checksum.json](https://github.com/qualifio/kibana-prometheus-exporter/releases/download/8.15.3/checksum.json) | [kibana-prometheus-exporter-8.15.3](https://github.com/qualifio/kibana-prometheus-exporter/releases/tag/8.15.3) |
| 8.15.0 | [checksum.json](https://github.com/qualifio/kibana-prometheus-exporter/releases/download/8.15.0/checksum.json) | [kibana-prometheus-exporter-8.15.0](https://github.com/qualifio/kibana-prometheus-exporter/releases/tag/8.15.0) |
| 8.14.3 | [checksum.json](https://github.com/qualifio/kibana-prometheus-exporter/releases/download/8.14.3/checksum.json) | [kibana-prometheus-exporter-8.14.3](https://github.com/qualifio/kibana-prometheus-exporter/releases/tag/8.14.3) |
| 8.14.2 | [checksum.json](https://github.com/qualifio/kibana-prometheus-exporter/releases/download/8.14.2/checksum.json) | [kibana-prometheus-exporter-8.14.2](https://github.com/qualifio/kibana-prometheus-exporter/releases/tag/8.14.2) |
| 8.14.1 | [checksum.json](https://github.com/qualifio/kibana-prometheus-exporter/releases/download/8.14.1/checksum.json) | [kibana-prometheus-exporter-8.14.1](https://github.com/qualifio/kibana-prometheus-exporter/releases/tag/8.14.1) |
| 8.14.0 | [checksum.json](https://github.com/qualifio/kibana-prometheus-exporter/releases/download/8.14.0/checksum.json) | [kibana-prometheus-exporter-8.14.0](https://github.com/qualifio/kibana-prometheus-exporter/releases/tag/8.14.0) |
| 8.13.4 | [checksum.json](https://github.com/qualifio/kibana-prometheus-exporter/releases/download/8.13.4/checksum.json) | [kibana-prometheus-exporter-8.13.4](https://github.com/qualifio/kibana-prometheus-exporter/releases/tag/8.13.4) |
| 8.13.3 | [checksum.json](https://github.com/qualifio/kibana-prometheus-exporter/releases/download/8.13.3/checksum.json) | [kibana-prometheus-exporter-8.13.3](https://github.com/qualifio/kibana-prometheus-exporter/releases/tag/8.13.3) |
| 8.13.2 | [checksum.json](https://github.com/qualifio/kibana-prometheus-exporter/releases/download/8.13.2/checksum.json) | [kibana-prometheus-exporter-8.13.2](https://github.com/qualifio/kibana-prometheus-exporter/releases/tag/8.13.2) |
| 8.13.1 | [checksum.json](https://github.com/qualifio/kibana-prometheus-exporter/releases/download/8.13.1/checksum.json) | [kibana-prometheus-exporter-8.13.1](https://github.com/qualifio/kibana-prometheus-exporter/releases/tag/8.13.1) |
| 8.13.0 | [checksum.json](https://github.com/qualifio/kibana-prometheus-exporter/releases/download/8.13.0/checksum.json) | [kibana-prometheus-exporter-8.13.0](https://github.com/qualifio/kibana-prometheus-exporter/releases/tag/8.13.0) |
| 8.12.2 | [checksum.json](https://github.com/qualifio/kibana-prometheus-exporter/releases/download/8.12.2/checksum.json) | [kibana-prometheus-exporter-8.12.2](https://github.com/qualifio/kibana-prometheus-exporter/releases/tag/8.12.2) |
| 8.12.1 | [checksum.json](https://github.com/qualifio/kibana-prometheus-exporter/releases/download/8.12.1/checksum.json) | [kibana-prometheus-exporter-8.12.1](https://github.com/qualifio/kibana-prometheus-exporter/releases/tag/8.12.1) |
| 8.12.0 | [checksum.json](https://github.com/qualifio/kibana-prometheus-exporter/releases/download/8.12.0/checksum.json) | [kibana-prometheus-exporter-8.12.0](https://github.com/qualifio/kibana-prometheus-exporter/releases/tag/8.12.0) |

<p align="center">For releases older than 8.12.0 please see: <a href="RELEASES.md">RELEASES.md</a></p>
