---
title: Batteries
---
{% error This site is in progress and is not yet complete. %}
If you have any question feel free to join the [Canberra Meshtastic Community](https://discord.com/invite/4QgFsuaC3Z) on Discord.
{% end %}

# Safety
Batteries when in an enclosure or by themselves are very safe.
However, there are lots of risks when modifying or attaching them to devices.
Below is a general list of things to keep an eye on when working with batteries.

## Always check polarity
It doesn't matter if it's your first time or your hundredth time, you always need to check the polarities when plugging in batteries.
Different revisions of the same device or different purchases of the same battery can have different wires connected to the same plugs.
Before plugging in a battery triple check which connectors are positive and negative on both the battery and device.
If you cross the positive and negative in a best case scenario your device is dead, at a worse case scenario your battery can catch on fire.

This cannot be stated enough **CHECK THE POLARITY**.

## Check for protection circuits
If you are sourcing Li-ion or Lipo batteries not all of them have protection circuits.
It is highly recommended that you purchase batteries with overcharge/discharge and anti-short circuit protection.
This will protect you and your devices if you make any mistakes.

## Do not buy the cheapest battery you find
Unlike most electronic products batteries can cause direct harm to you and your surroundings.
There is not only the scam aspect of the battery might not have as much capacity as expected but they can also have cheap or faulty protections.

## Check the battery type
This is only applicable to Li-Ion and Lipo batteries.
Most if not all Meshtastic devices are designed to accept a single cell 3.7V battery.
While you can buy multi cell batteries most Meshtastic devices are not designed for higher voltage.

## Check your battery voltage
This is only applicable to Li-Ion and Lipo batteries.
Use a multimeter to check the voltage of your batteries before plugging them into a device.
If your battery is below 3.0V or above 4.2V it is not safe to use, please dispose of it at a local battery recycler.
If you are storing your battery long term (1 month plus) charge or discharge your battery to 3.8V (~45%).

**If you are making parallel battery packs make sure all the batteries have the same voltage and capacity.**
Failure to do so can lead to rapid combustion of the pack.

## Purchase from your country
This is more of a guideline rather than a rule.
Not only will it be cheaper and faster to ship but shops inside your country will have higher standards of product control than overseas sites.

# Types of batteries
There are three types of batteries used with Meshtastic devices; battery packs, LiPo, and Li-ion.

## Battery packs
Battery packs are the easiest and safest batteries to use with Meshtastic.
They are normally used for recharging phones but since most Meshtastic devices have USBC or micro USB they are perfect for powering them.
Another added benefit is most battery packs have inbuilt anti overcharge/discharge features and have inbuilt protection for short circuits.
There is one big downside, because they don't use the onboard charging module (if the device has one) Meshtastic will be unable to advise of the power level.
This shouldn't be an issue for portable/handheld devices but is an issue if you want to properly monitor remote nodes.


## LiPo batteries
Most Meshtastic devices have charging circuits for LiPo batteries which means you will have access to the battery percent logs.
These batteries are also generally flat making them desirable for portable/handheld devices.

## Li-Ion batteries
Most Meshtastic devices have charging circuits for Li-Ion batteries which means you will have access to the battery percent logs.
These batteries are generally used are the standard [18650 size](https://en.wikipedia.org/wiki/18650_battery) which can be salvaged from laptops and cars.
18650 batteries are widely used in the maker community and in things like high powered flash lights.
Because of the form factor of the 18650, there are many housing units you can buy and 3D print making it easy to swap them out and make battery packs with.

# Battery sizing
The question everyone will ask is how many mAh should I get?
There is no easy answer to this unfortunately there is no easy answer to this.
Your device will draw vastly different power depending on the design, radio settings, antenna and radio traffic.
For handheld/portable devices 1,000-2,000 mAh is a good starting point.
Most solar devices will have 6,000+ mAh batteries or battery packs.
This is so they can last multiple days without solar charge in case of storms or cloudy weeks.
The best way to know what size battery to use is to test one in the location you want to deploy it in and keep an eye on the battery logs.
