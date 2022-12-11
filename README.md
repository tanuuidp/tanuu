# tanuu-idp
Tanuu Internal Development Platform Template

## Overview
For a description, please see [tanuu](https://tanuu.fi)

This repo contains templates to be used when implimenting your own IDP, based on Tanuu.

The [Tanuu-cli (under development)](https://github.com/tanuuidp/tanuu-cli) can be used to bootstrap a management cluster, it will use this repository as a source to deploy the components.

## Manual installation
If not using the cli, these are the steps to install tanuu toolset into an existing kubernetes cluster

```
kubectl apply -f bootstrap/namespaces.yaml
kubectl apply -f crds/
kubectl apply -f bootstrap/argocd.yaml
kubectl apply -f bootstrap/argosetup.yaml  
```

### Backstage setup/install
First, a secret named 'backstage-secret' should be created with env variables used for github use in backstage.
NOTE: Near term roadmap will move this into Vault.

Once the secret exists: 
```
kubectl apply -f setup/backstage/
```
