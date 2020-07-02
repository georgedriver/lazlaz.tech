# k8s-bundle - NGINX Ingress

This is the documentation for the NGINX Ingress Controller.

It is built around the [Kubernetes Ingress resource](https://kubernetes.io/docs/concepts/services-networking/ingress/), using a [ConfigMap](https://kubernetes.io/docs/tasks/configure-pod-container/configure-pod-configmap/#understanding-configmaps-and-pods) to store the NGINX configuration.

Learn more about using Ingress on [k8s.io](https://kubernetes.io/docs/concepts/services-networking/ingress/).

## Goals

We want to expose the L7 services with NGINX Ingress Controller, in order to support https protocal, we will install the [cert-manager](https://cert-manager.io/docs/) to interact with [alicloud DNS service](https://www.alibabacloud.com/product/dns) to auto create the https certificates from [Let's encrypt it](https://letsencrypt.org).

Below helm charts should be installed.

## nginx-ingress-docker-for-mac

Homepage: [https://github.com/georgedriver/helm-charts/tree/master/charts/nginx-ingress-docker-for-mac](https://github.com/georgedriver/helm-charts/tree/master/charts/nginx-ingress-docker-for-mac)

It's only used for installing the ingress controller for Kubernetes on docker for mac, thanks to the official [Installation Guide](https://kubernetes.github.io/ingress-nginx/deploy/#docker-for-mac), it also can be installed on Docker for Mac with a single [deploy.yaml](https://raw.githubusercontent.com/kubernetes/ingress-nginx/master/deploy/static/provider/cloud/deploy.yaml) file, but it doesn't have the helm chart for it, so I built it for it.

The nginx class name is `nginx`.

## cert-manager

cert-manager runs within your Kubernetes cluster as a series of deployment resources. It utilizes [`CustomResourceDefinitions`](https://kubernetes.io/docs/concepts/extend-kubernetes/api-extension/custom-resources) to configure Certificate Authorities and request certificates.

Homepage: [https://cert-manager.io/docs/installation/kubernetes/](https://cert-manager.io/docs/installation/kubernetes/)

If you install this cert-manager into your Kubernetes, you must also need to installed below \[georgedriver/alidns-webhook\]\([https://github.com/georgedriver/helm-charts/tree/master/charts/alidns-webhook](https://github.com/georgedriver/helm-charts/tree/master/charts/alidns-webhook)\) chart as well.

## alidns-webhook

Homepage: [https://github.com/georgedriver/helm-charts/tree/master/charts/alidns-webhook](https://github.com/georgedriver/helm-charts/tree/master/charts/alidns-webhook)

I build this helm chart based on \[pragkent/alidns-webhook\]\([https://github.com/pragkent/alidns-webhook](https://github.com/pragkent/alidns-webhook)\),  it has a lot of defects, please DO NOT use this in your production environment.

{% hint style="danger" %}
You must install jetstack/cert-manager before installing this helm chart, otherwise some unknown CRD errors will show up.
{% endhint %}



