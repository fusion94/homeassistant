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
