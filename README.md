# docker-celery-exporter

[![release](https://github.com/Intellection/docker-celery-exporter/actions/workflows/release.yml/badge.svg)](https://github.com/Intellection/docker-celery-exporter/actions/workflows/release.yml)
[![test](https://github.com/Intellection/docker-celery-exporter/actions/workflows/test.yml/badge.svg)](https://github.com/Intellection/docker-celery-exporter/actions/workflows/test.yml)

Docker image for [`danihodovic/celery-exporter`](https://github.com/danihodovic/celery-exporter), a Prometheus exporter for Celery metrics.

## Motivations

### How does this differ from upstream?

The current Docker image doesn't support ARM and we needed one that does. And [the review to add support](https://github.com/danihodovic/celery-exporter/pull/329) took longer than we could wait.

## Usage

```
docker run --name celery-exporter zappi/celery-exporter:latest
```

For more detailed usage documentation [see upstream](https://github.com/danihodovic/celery-exporter).
