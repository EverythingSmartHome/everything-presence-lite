---
layout: default
title: Connecting Home Assistant
nav_order: 1
parent: Home Assistant
---

# Connecting Home Assistant

{: .no_toc }

The final step is to connect to Home Assistant!
{: .fs-6 .fw-300 }

## Connecting to Home Assistant (Automatic method)

For most people, Home Assistant will automatically discover and add the EPL immediately, thanks to ESPHome's mDNS discovery.

To add it to Home Assistant, simply head to Settings > Devices and Services and you should see the Everything Presence Lite has been automatically discovered and is displayed - simply hit the configure button to add it to Home Assistant and that's it!

![Connecting the Lite to Home Assistant](../images/connecting-home-assistant-auto-1.png)
![Connecting the Lite to Home Assistant](../images/connecting-home-assistant-auto-2.png)

## Connecting to Home Assistant (Manual method)

If for some reason the Everything Presence Lite is not automatically discovered, or your network is not setup for mDNS you can add the Lite manually to Home Assistant.

You will need to first figure out what the IP address of your Lite is by checking your routers web page:

![Find the IP address in your router](../images/connecting-home-assistant-router-ip-address.png)

You can also use a program like [fing](https://www.fing.com) to discover network devices.

Once you have the IP address, head over to Home Assistant and go to Settings > Devices and Services and click the add Integration button in the bottom right.

![Connecting the Lite to Home Assistant](../images/connecting-home-assistant-manual-1.png)

Search for ESPHome to add an ESPHome device, and then enter the IP address into the box:

![Connecting the Lite to Home Assistant](../images/connecting-home-assistant-manual-2.png)

Hit next and finish, and the Lite is now connected to Home Assistant.

![Connecting the Lite to Home Assistant](../images/connecting-home-assistant-manual-3.png)

## Next Steps

Setup is now finished and you can go ahead and get automating the Everything Presence Lite! 🥳

If you would like a bit more information about what each entity does inside of Home Assistant, check out the Entities Explained page.

[Entities Explained](./home-assistant-entities.html){: .btn .btn-blue }

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
