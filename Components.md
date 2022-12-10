# External projects/components used
## Crossplane
Crossplane is a kubernetes custom resource defenition tool, allowing complex and elaborate kubernetes dependencies and objects be defined in a short consise yaml file. A kubernetes application deployment consists of several kubernetes objects: Deployment, Service, Horizontal Pod Autoscaller, Ingress, ConfigMaps, Secrets, and possibly more. Crossplane allows defines all of these, according to policies and best practices of the organization, and exposes them in a simple consice few lines of yaml, which is all the developers need to define.
[Crossplane](https://crossplane.io)

[Crossplane Github](https://github.com/crossplane/crossplane)

Crossplane License [Apache](https://github.com/crossplane/crossplane/blob/master/LICENSE)

## Backstage
Replaces manual cloning of git repository, and editing of settings/options for each new app with a templated model, including also the pipeline generation.

Initially a template creation tool. Automated documentation and link generation may be added. Backstage will not be essential to deployed applications. It is used primarily for instantiating new applications based on templates, and visibilty of the overall catalogs.
[Backstage.io](https://backstage.io)

[Backstage Github](https://github.com/backstage/backstage)

License [Apache](https://github.com/backstage/backstage/blob/master/LICENSE)

## Rancher server
Used primarily for the cenralized RBAC configuration of all k8s access, auditing of the access, and the transparent proxy of remote connections.

[Rancher](https://www.rancher.com/products/rancher) automates adding users (based on AD groups) in kubernetes clusters, and removes the need to manually adding users to new environments. All access to kubernetes would be managed via Rancher, and based only on AD group membership. Multifactor authentication set in AD would apply to all connections to environments. Rancher also allows users to use a reverse proxy tunnel to applications running inside isolated managed environments, without need for complex SSH tunneling or firewall updates. Rancher also maintains an audit log of all connections and actions, to every environment, by every user.

[Rancher Github](https://github.com/rancher/rancher)

License: [Apache](https://github.com/rancher/rancher/blob/master/LICENSE)

## ArgoCD
Used to keep k8s in sync with git repo, managing kubernetes as gitops.

Ensures that environments are always running in sync with defined state in GIT, without cron style ‘check’ jobs. The kubernetes/gitops model allows ‘self healing’ of environments, as the kubernetes contoller will be checking actual vs desired state (as defined in git) and always updating to desired. This improves uptime and reliability, and gives greater visibility to the actual state of environments.
[ArgoCD](https://argoproj.github.io/cd)

[ArgoCD Github](https://github.com/argoproj/argo-cd)

ArgoCD License [Apache](https://github.com/argoproj/argo-cd/blob/master/LICENSE)

## Arogo Workflows and Events
The primary job orchestration engine. Used for running the CI, building containers, running automated tests, security scans, and triggering deployments.

Due to its native kubernetes mindset and baseline, this replaces jenkins workflows with a modern, simplified, more atomic feature set.
[Workflows](https://argoproj.github.io/workflows)

[Workflows Github](https://github.com/argoproj/argo-workflows)

Workflows License [Apache](https://github.com/argoproj/argo-workflows/blob/master/LICENSE)

[Events](https://argoproj.github.io/events)

[Events Github](https://github.com/argoproj/argo-events)

Events License [Apache](https://github.com/argoproj/argo-events/blob/master/LICENSE)