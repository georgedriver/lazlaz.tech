---
description: >-
  It's an opinionated set of K8S configurations and applications running on top
  of a K8S cluster that abstract cloud provider specifics and provide additional
  features to build on top.
---

# k8s-bundle - overall introduction

The [k8s-bundle](https://github.com/georgedriver/k8s-bundle) is a [helmfile](https://github.com/roboll/helmfile) project that helps us to manage the applications \(ELK/Prometheus/Ingress, etc\) running on top of our K8S. These applications will be used to support our own applications' runtime.

## Goals

* Setup helm & helmfile environment
* Install the k8s-bundle
* Learn about the applications in k8s-bundle

## Setup helm & helmfile environment

* [helm](https://github.com/helm/helm): v3.2.3
* [helmfile](https://github.com/roboll/helmfile): v0.118.7

Or just using my docker image [k8s-tools](https://github.com/georgedriver/devops-tools/tree/master/k8s-tools) to setup your k8s-bundle.

* `docker pull georgedriver/k8s-tools`

## Install the k8s-bundle

* Clone the [k8s-bundle](https://github.com/georgedriver/k8s-bundle) repo

```text
git clone https://github.com/georgedriver/k8s-bundle.git
```

* `make install`

```text
cd k8s-bundle
make install
```

Please check more about helmfile from its [GitHub repo](https://github.com/roboll/helmfile#cli-reference).

## \[Option\] Learn about the applications in k8s-bundle

If you want to know the applications in my k8s-bundle, this section will show you the general infomation about it.

### Helmfile layout

{% hint style="info" %}
Please learn more from[`The Helmfile Best Practices Guide`](https://github.com/roboll/helmfile/blob/master/docs/writing-helmfile.md)\`\`
{% endhint %}

```text
k8s-bundle
.
├── CHANGELOG.md
├── README.md
├── environments
│   └── dev.yaml.gotmpl
│   └── prod.yaml.gotmpl
├── helmfile.yaml
└── values
```

* `environments` fold holds the environment related variables
  * We can refer to the [`Environment`](https://github.com/roboll/helmfile#environment) variables in  `helmfile.yaml`
  * Helmfile provides a `--environment NAME` flag to use the files in this folder like `helmfile --environment k8s-mirana sync`
* `helmfile.yaml`: The default name for a helmfile
  * Refer to the [helmfile configuration](https://github.com/roboll/helmfile#configuration) for more configs
  * `environments`: This section refers the `environment name` from the `environments` folder
  * `repositories` : This is the helm repos we're using later in `releases` section
  * `helmDefaults`: Default values to set for args along with dedicated keys that can be set by contributors
  * `releases`: The desired states of Helm releases, where we built the real helm applications
* `values`: Value files passed via `--values`

### Repositories

I'm trying to use the applications' official repositories as many as I can, if some applications do not have the official repositories, I will create it in my github helm charts: [**georgedriver \| helm-charts**](https://github.com/georgedriver/helm-charts), you're also welcomed to contribute your applications.

```text
repositories:
  - name: georgedriver
    url: https://georgedriver.github.io/helm-charts
```

I will introduce each applications in next pages, please note it's not guaranteed to keep it update, you should always to find the latest applications from [k8s-bundle](https://github.com/georgedriver/k8s-bundle/blob/master/helmfile.yaml) repo.

### 

#### 

