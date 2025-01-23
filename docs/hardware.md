---
title: Hardware
---
{% error This is site in progress and is not yet complete. %}
If you have any question feel free to join the [Canberra Meshtastic Community](https://discord.com/invite/4QgFsuaC3Z) on Discord.
{% end %}

# __Hardware__
The thing that makes Meshtastic work are microcontrollers with Lora boards.
Without it, you will not be able to communicate with other Meshtastic devices.
This will be broken up into a few classes of devices to make it easier to figure out what device suits you the best.
For a full listing of supported hardware and their details please look at the [Meshtastic website](https://meshtastic.org/docs/hardware/devices/).

## Starting devices
These devices are by no means less capable then any other devices on this list.
What makes them good starting device is they are widely used, have first class support from meshtastic and most importantly cheap.

### [Heltech Lora 32 V3](https://www.aliexpress.com/item/1005007752194012.html?spm=a2g0o.productlist.main.5.4b87AdHvAdHvtk&algo_pvid=5a198db4-b864-47ff-a07c-ced66078d83a&algo_exp_id=5a198db4-b864-47ff-a07c-ced66078d83a-2&pdp_npi=4%40dis%21AUD%2158.09%2130.79%21%21%21260.96%21138.32%21%402101ef5e17375454970241241e808a%2112000042088422265%21sea%21AU%212854040288%21X&curPageLogUid=csDpeljGXr73&utparam-url=scene%3Asearch%7Cquery_from%3A)
![Heltech Lora 32 V3](/images/heltec-lora-v3.png)
Most people will start with this device, it's cheap, comes with a case and antenna and it works.
The first thing you will notice in the Antanna is horrible, to make the device usable you will need an IPX to SMA adaptor so you can use an Antanna that works.
Outside of that it's a perfect device to start with.
Below are some case recommendations for it, all require a 3d printer and extra parts.
- [Heltec v3 case for Meshtastic](https://www.printables.com/model/561389-heltec-v3-case-for-meshtastic)
- [TacBox Meshtastic Case for Heltec V3](https://www.printables.com/model/991479-tacbox-meshtastic-case-for-heltec-v3)
- [Meshtastic with MagSafe](https://www.printables.com/model/806280-meshtastic-with-magsafe)

### [LILYGO TTGO](https://www.aliexpress.com/item/32872078587.html?spm=a2g0o.store_pc_allItems_or_groupList.0.0.27d3757bpUszIc&pdp_npi=4%40dis%21AUD%21AU%20%2439.83%21AU%20%2429.67%21%21%2124.58%2118.31%21%402103205117375477463775859e9c42%2112000036680562363%21sh%21AU%212854040288%21X&_gl=1*1f3l2h3*_gcl_aw*R0NMLjE3MzY3MzAxNzUuQ2p3S0NBaUE3WTI4QmhBbkVpd0FBZE9KVVA0alM1c0NHbWFfTW00ZDdvNEtaS1prRnhFUlFVU01BR2QyNHF5V3FHdkY0NVJwcGcwcjNCb0NBMUVRQXZEX0J3RQ..*_gcl_dc*R0NMLjE3MzY3MzAxNzUuQ2p3S0NBaUE3WTI4QmhBbkVpd0FBZE9KVVA0alM1c0NHbWFfTW00ZDdvNEtaS1prRnhFUlFVU01BR2QyNHF5V3FHdkY0NVJwcGcwcjNCb0NBMUVRQXZEX0J3RQ..*_gcl_au*NDkwOTIxNzcuMTczNTQzNzUxNw..*_ga*MzgwNTc0OTAzLjE3MzU0Mzc1MTg.*_ga_VED1YSGNC7*MTczNzU0NzcxNC45LjEuMTczNzU0Nzc1My4yMS4wLjA.)
All the upsides of the Heltek Lora 32 with the added benefit of having a full sized SMA connector.
The antennas are again not great so you will need a new one to properly use it but you will not need an adaptor.

## [NRF52 devices (Rak Wireless)](https://www.iot-store.com.au/collections/rak-wireless)
NRF52 devices are on the more expensive side of Meshtastic devices.
The upside of them is the extreme power efficiency.
Most repeaters in Canberra and NRF52 devices with solar panels as they can last for long periods with low solar power.
The radio module is also very good on these devices and has improved range over the other devices.
One of the downsides of this power efficiency is the microcontroller isn't as powerful as an ESP32-based system.
If you are doing things connecting your mestatic device to WiFi and JSON encoding the messages NRF52 devices are not the best for that.

## [LilyGo Tdeck and Tdeck plus](https://www.aliexpress.com/item/1005005692235592.html?spm=a2g0o.productlist.main.3.6bdb4ee1xw17w5&algo_pvid=6b2eba67-bf4a-43a6-826b-2dca8732afca&algo_exp_id=6b2eba67-bf4a-43a6-826b-2dca8732afca-1&pdp_npi=4%40dis%21AUD%2192.70%2176.09%21%21%2157.21%2146.96%21%402103244617375497343524113e0bb7%2112000037262377166%21sea%21AU%212854040288%21X&curPageLogUid=uf6zjuPknzjD&utparam-url=scene%3Asearch%7Cquery_from%3A)
Tdeck's get their own entry as they have a few downsides that you need to be aware of before you purchase them.
Tdeck's are officially supported by Meshtastic with the base firmware, however this firmware will not give you the full GUI and touchscreen support.
To get full GUI support you need to flash the [tft-gui-work branch](https://github.com/meshtastic/firmware/tree/tft-gui-work) of the firmware.
This firmware is beta and not officially supported.
**DO NOT** follow guides that tell you to download firmware files and change the partition tables.
This method is not supported by Meshtastic and they are very diligent in deleting firmware files from the automated build process.
To flash the firmware you must clone the repo to your computer, change the branch to tft-gui-work and use VScode to build and flash the firmware.
Full details on the process can be found in the below link.
https://meshtastic.org/docs/development/firmware/build/
https://meshtastic.org/docs/getting-started/flashing-firmware/
As long as you are prepared to get your hands dirty this is a very capable device and the novelty of having a BlackBerry like device that you can communicate with is great.
