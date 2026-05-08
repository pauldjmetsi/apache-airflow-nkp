# Apache Airflow Setup 

This is a simple example of how to setup Apache Airflow using Helm and Flux.

## Steps 

1. Pull the repository down to you machine where you run kubectl commands
2. Run the following command to install the helm repositories and git repositories
```
kubectl apply -k infrastructure/
```
3. Run the following command to install Apache Airflow to the dev cluster
```
kubectl apply -f clusters/dev/flux-kustomization.yaml
```

## Flow 

1. kubectl apply -k infrastructure/          
    1.1 == GitRepository and HelmRepository created 
2. kubectl apply -f flux-kustomization.yaml  
    2.1 == Flux watches ./clusters/dev
3. clusters/dev/kustomization.yaml           
    3.1 == namespace.yaml and helmrelease.yaml applied
4. helmrelease.yaml                          
    4.1 == Airflow Helm chart installed

