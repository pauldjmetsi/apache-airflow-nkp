# Apache Airflow Setup 

This is a simple example of how to setup Apache Airflow using Helm and Flux.

## Steps 

1. Pull the repository down to you machine where you run kubectl commands
2. Run 'kubectl apply -k infrastructure/' to install the helm repositories and git repositories
3. Run 'kubectl apply -f clusters/dev/flux-kustomization.yaml' to install Apache Airflow to the dev cluster
