# 00 OS Installation

## What do I have

* Sony 61212t
* USB flash disk \(8GB\)

## Objective

Install Ubuntu desktop 18.04.4 LTS on Sony 61212t.

## Steps

### OS installation

* Download Ubuntu Desktop 18.04.4 LTS from its official site [https://ubuntu.com/download/desktop](https://ubuntu.com/download/desktop)
* Flash image to USB drive with [https://www.balena.io/etcher/](https://www.balena.io/etcher/)

### OS initialization

* Enable ssh service

```text
sudo apt-get update
sudo apt-get install openssh-server
```

* Disable "HandleLidSwitch"

{% embed url="https://blog.csdn.net/xiaoxiao133/article/details/82847936" %}



