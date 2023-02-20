# selfcare-aks-cert-mounter

This project allows to load certificate from KV, that must be used be ingress

## Blue print source

see. <https://github.com/pagopa/aks-helm-cert-mounter-blueprint> as source for this project

## Init project

```sh
helm repo add cert-mounter-blueprint https://pagopa.github.io/aks-helm-cert-mounter-blueprint
```

## Launch project (from domain folder e.g.: helm/pnpg)

### 1️⃣ Install dependencies

this must be done the first time or every time that you change the chart source

```sh
helm dep build
```

### 2️⃣ Execute the installation

```sh
helm upgrade -i -n <namespace name> -f <file with values> <name of the helm chart> <chart folder>

helm upgrade -i -n pnpg -f values-dev.yaml cert-mounter \. --debug
```
