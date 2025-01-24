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
## Rust
[https://github.com/meshtastic/rust](https://github.com/meshtastic/rust)
## Typescript (Website)
[https://github.com/meshtastic/web](https://github.com/meshtastic/web)

# Monitoring
Many people in the community like to monitor and keep a close eye on the network to find issues and help with planning out the network.
Most of these tools require an MQTT server that you connect your Meshtastic node too, some allow you to use blue tooth or USB.

## Meshtastic Prometheus Exporter
This software is used a lot by the community, built off Grafana, Prometheus, Redis and a MQTT server.

[https://github.com/tcivie/meshtastic-metrics-exporter](https://github.com/tcivie/meshtastic-metrics-exporter)

## Mesh Sense
Mesh Sense is an application much like the Meshtastic Prometheus Exporter, however it runs as a local app not as a large server application.
You can directly connect to your device over Bluetooth or WiFi.

[https://github.com/Affirmatech/MeshSense](https://github.com/Affirmatech/MeshSense)

# Node planning
Part of building a network is know where to put a new node.
Most of the figuring out when a new node is needed is done by looking at the data from the monitoring tools.
But when you have identified when you need a new node you need to find the best spots that will give the furthest reach.
Blew are some tools that are used.

## Meshtastic Site planner
The Meshtastic Site planner is the default go to that will allow you to run simulations on range and topology.
[https://site.meshtastic.org/](https://site.meshtastic.org/)
