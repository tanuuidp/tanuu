# Setup

Here is where we keep all the tools installed. This is managed with argoCD gitops. The ArgoCD is installed in the bootstrap directory.

Argoproj tools are installed from argo-events and workflow-install. The pipelines and event listeners used inside argo are setup in the argo-config directory.

When adding new components, be sure to add the argo app in argo-applications, so gitops will deploy and manage it.