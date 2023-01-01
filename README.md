[![GitHub stars](https://img.shields.io/github/stars/fusion94/homeassistant.svg?style=plasticr)](https://github.com/geekofweek/homeassistant/stargazers)
[![GitHub last commit](https://img.shields.io/github/last-commit/fusion94/homeassistant.svg?style=plasticr)](https://github.com/fusion94/homeassistant/commits/master)
![GitHub commit activity](https://img.shields.io/github/commit-activity/w/fusion94/homeassistant)
[![HA Version](https://img.shields.io/badge/Running%20Home%20Assistant-2022.12.7%20-darkblue)](https://github.com/home-assistant/home-assistant/releases/latest)
[![HA Community](https://img.shields.io/badge/HA%20community-forum-orange)](https://community.home-assistant.io/u/fusion94/summary)
![GitHub](https://img.shields.io/github/license/fusion94/homeassistant)

# Overview

My personal [Home Assistant Container](https://home-assistant.io)
configurations.

I utilize Home Assistant to bridge and automate all my home automation products.
It was quickly realized as I expanded beyond some smart bulbs and a Hue hub,
that nothing integrated into a single system for control, automation, and
communication. Home Assistant originally was run on a Raspberry Pi but I have
since moved it to run as a docker container running on a [Synology NAS
DiskStation DS1621+](https://www.synology.com/en-us/products/DS1621+)

## Architecture

I'm running two internet connections here at the house. The first is
Xfinity/Comcast Business Internet Gigabit Extra (1.25 Gbps / 35 Mbps) and the
other is AT&T's Internet 100 (100 Mbps / 25 Mbps). Both of these routers are
plugged into a [Ubiquiti Security Gateway Pro
(USG-PRO-4)](https://store.ui.com/collections/routing-switching/products/unifi-security-gateway-pro)
which is rack mounted in my Garage/Home Office/Man Cave. You can configure the
USG-Pro to either do WAN Failover or WAN Load Balancing. I've configured the
USG-Pro-4 to utilize WAN Failover.

![USG-PRO-4](usg-pro-wan-full.png)
_USG-Pro-4 WAN Failover_

**What is WAN Failover?**
Failover enables you to connect a second Internet connection to your UniFi
Gateway which will serve as a “backup”. If your primary Internet service goes
down, you will begin utilizing your secondary Internet connection.

**How does UniFi determine if my Internet goes down?**
The UniFi Network Application checks for connectivity and latency to an “echo
server”. By default, this is set to ping.ui.com which leverages responses from
various locations to ensure maximum accuracy.

In addition to the two WAN connections, UniFi Gateways also support the use of
our UniFi LTE Backup which is connected to a LAN port. This is only capable of
being used as a failover option.

While I have the [UniFi
LTE](https://store.ui.com/collections/wireless/products/unifi-lte) I've yet to
configure it for use.

## Gear/Equipment

- Cloud Key Gen2 Plus running UniFi OS Version 3.0.13

## Screenshots

![HA Dashboard Overview](overview.png)
_Entry Point into the Dashboards_

![HA Dashboard - Synology](synology.png)
_Synology Dashboards_

## Features

- Turning on lights depending on the time of day (sunrise/sunset)
- Smoke Alarms/CO<sub>2</sub> Detection
- Printer low ink notification
- Doorbell notification
- Low battery on devices
- High humidity notification

**Note: Private information is stored in secrets.yaml (not uploaded)**
