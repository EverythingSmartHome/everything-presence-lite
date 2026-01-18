---
layout: default
title: Carbon Dioxide (CO2)
nav_order: 1
parent: Modules
---

# Integrating the CO2 module

{: .no_toc }

Add Carbon Dioxide monitoring to your Everything Presence Lite.
{: .fs-6 .fw-300 }

{: .important }
Please note the CO2 module is only compatible with Home Assistant.

## Hardware

First take your Lite (with it powered off!) and identify the GPIO pins in the bottom corner (depending on your board your revision, these may look slightly different):

![Everything Presence Lite GPIO Pins](https://everythingsmarthome.github.io/everything-presence-lite/images/everything-presence-lite-gpio-pins.jpg)

Grab your CO2 module and push it onto the pins, making sure to line up the 3.3v and Ground pins:

![Everything Presence Lite CO2 placement](https://everythingsmarthome.github.io/everything-presence-lite/images/everything-presence-co2-scd40-lite.jpg)

## Software

You will need to install the CO2 version of the firmware by heading over to the [update page](https://everythingsmarthome.github.io/everything-presence-lite/updating.html), selecting Home Assistant, select LD2450 (the default sensor), select CO2 and then choose between the Bluetooth or Non-Bluetooth versions of the firmware. Finally hit the Connect button and follow the instructions.

Once installed, the CO2 sensor should automatically show up in Home Assistant, nice!


<script>
const toggleDarkMode = document.querySelector('.js-toggle-dark-mode');

jtd.addEvent(toggleDarkMode, 'click', function(){
  if (jtd.getTheme() === 'dark') {
    jtd.setTheme('light');
    toggleDarkMode.textContent = 'Preview dark color scheme';
  } else {
    jtd.setTheme('dark');
    toggleDarkMode.textContent = 'Return to the light side';
  }
});
</script>
