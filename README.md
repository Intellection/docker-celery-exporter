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

## Releasing

To cut a new release, follow these steps:

1. Ensure your local `main` branch is up to date:
    ```bash
    git checkout main
    git fetch origin main
    ```
2.	Create a signed tag for the new release replacing <x.y.z> with the version you’re releasing:
    ```bash
    git tag -s <x.y.z> -m "Version <x.y.z>"
    ```
3. Push the newly created tag to the remote repository:
    ```bash
    git push origin <x.y.z>
    ```
