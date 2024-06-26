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

You will need the ESPHome add-on installed in Home Assistant and the code for your Everything Presence Lite adopted (you should be automatically prompted to do this if you haven't already done so).

Once you have your config showing up in the ESPHome dashboard, hit edit on the config.

Then at the bottom of the config, add the following lines:

```
i2c:
  - id: bus_a
    sda: 21
    scl: 22
    scan: true
  - id: bus_b
    sda: 26
    scl: 27
    scan: true

sensor:
  - id: !extend illuminance_sensor
    i2c_id: bus_a
  - platform: scd4x
    i2c_id: bus_b
    co2:
      name: "CO2"
```

Then hit save and install to complete.

{: .note }
If your ESPHome config produces an error when trying to install, try hitting the "clean build files" button on the config to clear your cache, then try again.

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
