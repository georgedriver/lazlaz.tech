---
description: Provide the Kubernetes playground for your self.
---

# 00 Goals

I'm going to introduce how to setup your own Kubernetes cluster for your home use. I will show you how to config a Kubernetes on a Mac mini, install software applications bundles \(aka [k8s-bundle](https://github.com/georgedriver/k8s-bundle)\) into the Kubernetes, and setup CI/CD pipeline to support your own apps.

## Goals

You can choose any below goals as your own goals according to your real demands.

* Create a Kubernetes cluster locally
* Learn the best practice \(for me for now\) to manage the helm packages
* Bring the k8s-bundle into the Kubernetes for as your Kubernetes' infrastructure
* Learn the CI/CD best practice for Kubernetes to support your own apps

## The necessary knowledge

* [Kubernetes](https://kubernetes.io) medium level management
* Know how to use the [helm](http://helm.sh) \(v3\) chart

## Configurations

![](../.gitbook/assets/image%20%285%29.png)

System Version: `macOS 10.15.2 (19C57)`  
Helm Version: `v3.2.4`

Docker for mac: `2.3.0.3 (45519) stable`

## \[Extra\] Home network topology

{% hint style="warning" %}
This is my home network topology for you to understand the whole system in this tutorial. You don't need to have the same configuration with me.
{% endhint %}

![](../.gitbook/assets/image%20%2819%29.png)



