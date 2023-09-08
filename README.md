# Instance Manager Tooling

The following is a quick guide on what you need to develop the DHIS2 instance manager.

## Prerequisites

### Tools

Install the following

* Go - https://go.dev/
* Interact with Kubernetes using kubectl - https://kubernetes.io/docs/tasks/tools/
* Kubernetes package manager - https://helm.sh/
* Encrypt/Decrypt secrets - https://github.com/mozilla/sops
* Encrypt/Decrypt secrets in Helm (using SOPS) - https://github.com/jkroepke/helm-secrets
* Build, push, deploy services to Kubernetes - https://skaffold.dev
* Deploy Kubernetes locally - [Kind](https://kind.sigs.k8s.io/docs/user/quick-start), [k3s](https://github.com/k3s-io/k3s), [minikube](https://minikube.sigs.k8s.io/docs/start/)

### Repositories

Clone the repos declared in `requires.path` [skaffold.yml](./skaffold.yaml)
satisfying the path locations.

## Build, Push And Deploy Instance Manager

Copy .env.example to .env

Update the `ENVIRONMENT` and `CLASSIFICATION` variables to match your environment.

Run `skaffold dev`

## Develop

Every repo you checked out has a `Makefile`. Consider this the entry point.

Start by calling

    make init

to setup [pre-commit hooks](https://pre-commit.com/). This ensures the code we
add follows some common conventions.

