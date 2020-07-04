# 01 The infrastructure

## Platform Infrastructure

![](../.gitbook/assets/image%20%2812%29.png)

## K8s-bundle

This is a home for K8S [_helmfiles_](https://github.com/roboll/helmfile)_._ 

It's a GitHub repo which contains the helmfiles provisioning the platform on top of an empty Kubernetes cluster and the configuration files for the K8S clusters/environments. 

It's an opinionated set of K8S configurations and applications running on top of a K8S cluster that abstract cloud provider specifics and provide additional features to build on top.

_See more in the GitHub repo_ [_**k8s-bundle**_](https://github.com/georgedriver/k8s-bundle)_\*\*\*\*_

### The fact of the k8s-bundle

| K | V |
| :--- | :--- |
| **Codename** | `k8s-mirana` |
| **Provider** | `docker-for-mac` |
| **Location** | cn-shanghai |
| **Environment** | dev |
| **Domain** | `mirana.cndriver.tech` |
| **Secret management** | \*\*\*\*[bank-vaults](https://github.com/banzaicloud/bank-vaults) |
| **Observability** | \*\*\*\*[Grafana](http://grafana.com)/[Prometheus](https://prometheus.io)/[Alertmanager](https://prometheus.io/docs/alerting/alertmanager/) |
| **Loadbalancer IP** | localhost \(127.0.0.1\) |
| **kubernetes.io/ingress.class** | `nginx` |
| **cert-manager.io/cluster-issuer** | `letsencrypt-prod` |

## 

