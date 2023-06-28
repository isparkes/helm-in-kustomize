# helm-in-kustomize

Proof of concept for ArgoCD using helm charts and merging secrets from a separate source. Our use case is that a software supplier delivers a Helm Chart containing the software, but we are responsible for the configuration and secrets management. We don't want to expose the secrets to the supplier.

We leverage kustomize to expand the Helm Chart and merge in our secrets. To build: 

    kustomize build . --enable-helm
