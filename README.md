# Helm-Charts-K8
When building and deploying applications, Helm Charts provide the ability to leverage Kubernetes packages through the click of a button or single CLI command. They provide a convenient way for developers to distribute applications, and for end users to install those applications.

Simple example to install prometheus with Helm Charts.

Steps followed:

*As Root*
```

1. Install Helm
$ snap install helm --classic

2. Install the repo, update it and install prometheus.
$ helm repo add prometheus-community https://prometheus-community.github.io/helm-charts 
$ helm repo update
$ helm install prom prometheus-community/prometheus

3. Uninstall Prometheus installed and intall it with custom values- by changing name of default alert manager and service type.
$ helm uninstall prom
4 helm install prom-1 prometheus-community/prometheus --set alertmanager.name=my-am --set server.service.type=NodePort

Quick tip-
Use the below command to list the default values for Prometheus installation-
$ helm show values prometheus-community/prometheus

```
*As Root*
