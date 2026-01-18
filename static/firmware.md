---
layout: default
title: Updating and Connecting to WiFi
nav_exclude: true
---

# Updating and Connecting To WiFi

{: .no_toc }

This page will help you to flash and update your Everything Presence Lite to the latest version and get it connected to WiFi!
{: .fs-6 .fw-300 }

## Everything Presence Lite ESPHome Firmware Install

Here you can install the latest [ESPHome](https://esphome.io) firmware on the Everything Presence Lite board for direct integration with [Home Assistant](https://home-assistant.io)

First, make sure you have the Lite connected to a USB port on your computer and select the platform you would like to install below. Hit the connect button, select the USB port from the list and then hit the install button to begin installing the latest software on your Everything Presence Lite.

Once the install has completed, you can then connect the Lite to your WiFi easily and securely.

{: .warning-title }
If you do not see a "Connect" button below, use a supported web browser like Google Chrome.

{: .warning-title }
After clicking the "Connect" button, if you do not see a "USB Serial" port listed, or you get the error "Failed to open serial port.", you may need to install the CH340 driver. The installer should give you links to the latest driver.

<div class="container">
    <div class="question-prompt">Select Smart Home Platform:</div>
    <div class="types">
        <label>
            <input type="radio" name="platform" value="HomeAssistant" />
            <div class="name">Home Assistant</div>
            <div class="description">Choose this for Home Assistant integration, with additional options for Bluetooth Proxy</div>
        </label>
    </div>

    <div id="homeAssistantOptions" class="hidden">
        <div class="question-prompt">Select Option:</div>
        <div class="types">
            <label>
                <input type="radio" name="haOption" value="Bluetooth" />
                <div class="name">Bluetooth Proxy</div>
                <div class="description">Choose this option to enable Bluetooth Proxy and Improv. Can cause connectivity issues with WiFi.</div>
            </label>
            <label>
                <input type="radio" name="haOption" value="NoBluetooth" />
                <div class="name">No Bluetooth</div>
                <div class="description">Choose this option to disable Bluetooth Proxy and Improv, which can improve stability of the WiFi connection and/or you don't need Bluetooth Proxy.</div>
            </label>
        </div>
    </div>

    <esp-web-install-button class="hidden"></esp-web-install-button>
</div>

<script
    type="module"
    src="https://unpkg.com/esp-web-tools@9/dist/web/install-button.js?module"
></script>

<script>
    document.querySelectorAll('input[name="platform"]').forEach(radio =>
        radio.addEventListener("change", function(event) {
            var selectedPlatform = event.target.value;
            var homeAssistantOptions = document.getElementById("homeAssistantOptions");
            var installButton = document.querySelector("esp-web-install-button");

            homeAssistantOptions.classList.add("hidden");
            installButton.classList.add("hidden");

            if (selectedPlatform === "HomeAssistant") {
                homeAssistantOptions.classList.remove("hidden");

                document.querySelectorAll('input[name="haOption"]').forEach(optionRadio =>
                    optionRadio.addEventListener("change", function() {
                        installButton.classList.remove("hidden");

                        if (this.value === "Bluetooth") {
                            installButton.setAttribute("manifest", "https://everythingsmarthome.github.io/everything-presence-lite/everything-presence-lite-ha-manifest.json");
                        } else if (this.value === "NoBluetooth") {
                            installButton.setAttribute("manifest", "https://everythingsmarthome.github.io/everything-presence-lite/everything-presence-lite-ha-no-ble-manifest.json");
                        }
                    })
                );
            }
        })
    );
</script>
