Drone plugin to build and upload Docker manifests. You are able to combine
different architectures of your Docker image within a single manifest.

## Examples

```yaml
kind: pipeline
name: default

steps:
- name: step name
  image: dronehippie/manifest:1
  settings: []
```

## Parameters

dummy
: dummy
