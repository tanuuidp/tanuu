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
kubectl apply -f crds/argocd-crds.yaml  
kubectl apply -f crds/event-crds.yaml 
kubectl apply -f crds/workflow-crds.yaml 


```
