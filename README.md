# manifest

[![Current Tag](https://img.shields.io/github/v/tag/dronehippie/manifest?sort=semver)](https://github.com/dronehippie/manifest) [![Build Status](http://drone.webhippie.de/api/badges/dronehippie/manifest/status.svg)](http://drone.webhippie.de/api/badges/dronehippie/manifest) [![Join the Matrix chat at https://matrix.to/#/#webhippie:matrix.org](https://img.shields.io/badge/matrix-%23webhippie-7bc9a4.svg)](https://matrix.to/#/#webhippie:matrix.org) [![Docker Size](https://img.shields.io/docker/image-size/dronehippie/manifest/latest)](https://hub.docker.com/r/dronehippie/manifest) [![Docker Pulls](https://img.shields.io/docker/pulls/dronehippie/manifest)](https://hub.docker.com/r/dronehippie/manifest) [![Go Reference](https://pkg.go.dev/badge/github.com/dronehippie/manifest.svg)](https://pkg.go.dev/github.com/dronehippie/manifest) [![Go Report Card](https://goreportcard.com/badge/github.com/dronehippie/manifest)](https://goreportcard.com/report/github.com/dronehippie/manifest) [![Codacy Badge](https://app.codacy.com/project/badge/Grade/fedbf740cb83476a908d290795cb4efa)](https://www.codacy.com/gh/dronehippie/manifest/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=dronehippie/manifest&amp;utm_campaign=Badge_Grade)

Drone plugin to build and upload Docker manifests. For the usage information and a listing of the available options please take a look at the [documentation](https://dronehippie.github.io/manifest/).

## Build

Build the binary with the following command:

```console
export GOOS=linux
export GOARCH=amd64

make build
```

## Docker

Build the image with the following command:

```console
docker build \
  --label org.opencontainers.image.source=https://github.com/dronehippie/manifest \
  --label org.opencontainers.image.revision=$(git rev-parse --short HEAD) \
  --label org.opencontainers.image.created=$(date -u +"%Y-%m-%dT%H:%M:%SZ") \
  --file docker/Dockerfile.amd64 --tag dronehippie/manifest .
```

## Usage

```console
docker run --rm \
  -e PLUGIN_DUMMY="dummy" \
  -v $(pwd):$(pwd) \
  -w $(pwd) \
  dronehippie/manifest
```

## Security

If you find a security issue please contact [thomas@webhippie.de](mailto:thomas@webhippie.de) first.

## Contributing

Fork -> Patch -> Push -> Pull Request

## Authors

-   [Thomas Boerger](https://github.com/tboerger)

## License

Apache-2.0

## Copyright

```console
Copyright (c) 2021 Thomas Boerger <thomas@webhippie.de>
```
