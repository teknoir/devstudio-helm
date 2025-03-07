# Devstudio Helm Chart

This chart deploys Devstudio to a Kubernetes cluster.

> The implementation of the Helm chart is right now the bare minimum to get it to work.

## Usage in Teknoir platform
Use the HelmChart to deploy the Devstudio to a Device.

```yaml
---
apiVersion: helm.cattle.io/v1
kind: HelmChart
metadata:
  name: devstudio
  namespace: default
spec:
  repo: https://teknoir.github.io/devstudio-helm
  chart: devstudio
  targetNamespace: default
  valuesContent: |-
    # Example for minimal configuration
    
```

## Adding the repository

```bash
helm repo add teknoir-devstudio https://teknoir.github.io/devstudio-helm/
```

## Installing the chart

```bash
helm install devstudio teknoir-devstudio/devstudio -f values.yaml
```