![build status](https://github.com/dpnl87/hugo-docker/workflows/Docker%20Image%20CI/badge.svg)

# Hugo docker

This is a custom Docker container for my [Hugo](https://gohugo.io/) setup. It is build from the Debian [stable-slim](https://hub.docker.com/_/debian) container and includes everything needed including [pygments](https://pygments.org/)

## Usage

To pull the image run:

```bash
❯ docker pull dpnl87/hugo-docker:latest
```

If you want to check the hugo version you can use:

```bash
❯ docker run dpnl87/hugo-docker:latest hugo version
Hugo Static Site Generator v0.55.5-A83256B9 linux/amd64 BuildDate: 2019-05-02T13:03:36Z
```

To run a Hugo development server you can run:

```bash
❯ docker run --rm --name danielpaulus.com -v "$(pwd)":/usr/share/blog -p 1313:1313 dpnl87/hugo-docker:latest hugo server -D -b http://localhost:1313 --bind=0.0.0.0
```
