# Hyperledger Helm Charts

## Component

### Fabric
- fabric-ca

## Quick Start

```shell
$ helm repo add hlcharts https://guanbo.github.com/hlcharts
```

as depency

```yaml
- name: fabric-ca
  version: x.x.x
  repository: https://guanbo.github.com/hlcharts/
  condition: fabric-ca.enabled
  tags:
    - hyperledger
```

## Howto build

```shell
$ helm create mychart
$ helm package mychart
$ mv mychart-0.1.0.tgz docs
$ helm repo index docs --url https://guanbo.github.com/hlcharts
$ git add -i
$ git commit -av
$ git push origin master
```