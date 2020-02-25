---
description: 树莓派折腾记
---

# Expose your internal service to the Internet

{% embed url="https://www.bilibili.com/video/av91123250/" %}

Let's expose your Deluge service on Raspberry Pi to the Internet

## Home network topology

![port-forward](../.gitbook/assets/home-network.png)

## What do I have

- Telecom SDN (modem)
- miwifi3g
- PPPoE account
- Raspberrypi 4B

## Objective

Using port forwarding feature on miwifi3g to expose the Deluge service to the Internet.

The deluge service can be accessed by:
- http://192.168.123.15:8112 [Intranet]
- http://[DDNS-HOST]:8112 [Internet]

## Steps

### Get the public IP address from your ISP

- Change modem working mode from "route" to "bridge"
- Dial PPPoE on miwifi3g with the account provided by your ISP

Recommended:
- Setup DDNS on miwifi3g to map the dynamic public IP

### - Setup Port Forwarding on miwifi3g

- port forwarding

### Connect your deluge service from anywhere

- Test the connection via DDDN domain + port
- Modify the Chrome plugins configuration to use the new public services
