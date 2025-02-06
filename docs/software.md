---
title: Software
---
{% error This site is in progress and is not yet complete. %}
If you have any question feel free to join the [Canberra Meshtastic Community](https://discord.com/invite/4QgFsuaC3Z) on Discord.
{% end %}

# Software
There is many different types of software for Meshtastic.
Most importantly being the [firmware](https://github.com/meshtastic/firmware).
The firmware and most software built around Meshtastic is opensource which means you can read it and contribute to it.

# Api's and Libraries
To build something to interact a Meshtastic device you can ether use a direct [serial](https://en.wikipedia.org/wiki/Serial_communication) or you can use a library to have more control and features.

Below is a list of libraries built for different languages that you can use in your project.

## Arduino
[https://github.com/meshtastic/Meshtastic-arduino](https://github.com/meshtastic/Meshtastic-arduino)
## C#
[https://github.com/meshtastic/c-sharp](https://github.com/meshtastic/c-sharp)
## Python
[https://github.com/meshtastic/Python](https://github.com/meshtastic/python)
* Python MQTT [paho-mqtt](https://pypi.org/project/paho-mqtt/)
## Rust
[https://github.com/meshtastic/rust](https://github.com/meshtastic/rust)
## Typescript (Website)
[https://github.com/meshtastic/web](https://github.com/meshtastic/web) 

# Misc
* **Docker** is an open-source platform that enables developers to build, deploy, run, update and manage containers. Containers are standardized, executable components that combine application source code with the operating system (OS) libraries and dependencies required to run that code in any environment.
* **JSON** (JavaScript Object Notation) is a text-based, human-readable data interchange format used to exchange data between web clients and web servers. Not available on all firmware on all devices, check if your device supports it before going down a rabbit hole.
* **MQTT** (Message Queuing Telemetry Transport) It is a lightweight messaging protocol for use in cases where clients need a small code footprint and are connected to unreliable networks or networks with limited bandwidth resources.
* **Protobuf** (Protocol Buffers) is a free and open-source cross-platform data format used to serialize structured data. [meshtastic protobuf definitions](https://github.com/meshtastic/protobufs)

# Location Tracking
* One solution is to follow this step by step docker based solution [meshtastic-and-owntracks](https://hackaday.com/2023/10/11/meshtastic-and-owntracks-to-kick-your-google-habit/) requires a JSON functioning device and the owntracks interface is a little clunky but funtional.

# Monitoring
Many people in the community like to monitor and keep a close eye on the network to find issues and help with planning out the network.
Most of these tools require an MQTT server that you connect your Meshtastic node too, some allow you to use blue tooth or USB.

## Home Assistant
If you have a home assitant (HASS) instance running at home, you might like to integrate your mesh devices for location, automation or messaging, theres a couple of different options.

* [homeassistant-meshtastic](https://github.com/broglep/homeassistant-meshtastic) is protobuf native speaking interface between HA & meshtastic installed and managed through HACS, allows local devices to be added as hubs and nodes to be added for location tracking, but does then use that interface (eg if you are accesssing your device by it's IP address, and then configure this add-on, to that IP, the device can't support two connections on the one interface, and they will constantly fight/disconnect) if you still have the BT interface enabled, you can connect with the phone app (for example).

* [hass_Mtastic_MQTT](https://github.com/kvj/hass_Mtastic_MQTT) also uses protobuf native, but goes via MQTT, most mildly complex HA installs will already have an MQTT server, so the usual MQTT config steps should work, alternately the link shows how to configure pulling public MQTT server data into your local instance.

* [mqtt_json](https://www.home-assistant.io/integrations/mqtt_json/) If you have a JSON capable device configured to deliver to your HA MQTT, there are resources available to create entities inside HA, probably most useful for specific use cases.

## Meshtastic Prometheus Exporter
This software is used a lot by the community, built off Grafana, Prometheus, Redis and a MQTT server.

[https://github.com/tcivie/meshtastic-metrics-exporter](https://github.com/tcivie/meshtastic-metrics-exporter)

## Mesh Sense
Mesh Sense is an application much like the Meshtastic Prometheus Exporter, however it runs as a local app not as a large server application.
You can directly connect to your device over Bluetooth or WiFi.

[https://github.com/Affirmatech/MeshSense](https://github.com/Affirmatech/MeshSense)

## MQTT enabling
This is the official MQTT reference [/module/mqtt/](https://meshtastic.org/docs/configuration/module/mqtt/) shows how to configure your device, and how to connect to the public MQTT server. If you prefer to play in your own private patch, it's relatively painless to set up a MQTT instance in a docker container on your local network, search for a phrase like 'MQTT broker using docker' and find an instruction set that speaks to you.
* [mqtt-explorer](http://mqtt-explorer.com/) is a super handy tool for browsing your MQTT broker.
* You need to enable mqtt uplink in your channel settings as well.

# Node planning
Part of building a network is know where to put a new node.
Most of the figuring out when a new node is needed is done by looking at the data from the monitoring tools.
But when you have identified when you need a new node you need to find the best spots that will give the furthest reach.
Blew are some tools that are used.

## Meshtastic Site planner
The Meshtastic Site planner is the default go to that will allow you to run simulations on range and topology.
[https://site.meshtastic.org/](https://site.meshtastic.org/)
