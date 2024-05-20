---
layout: default
title: Updating and Connecting to WiFi
nav_order: 4
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
            <input type="radio" name="platform" value="Home Assistant" />
            <div class="option-content">
                <img src="images/home-assistant-logo.png" alt="Home Assistant" class="option-image">
                <div>
                    <div class="title">Home Assistant</div>
                    <div class="description">Choose this for Home Assistant integration, with additional options for Bluetooth Proxy</div>
                </div>
            </div>
        </label>
    </div>

    <div id="sensorOptions" class="hidden">
        <div class="question-prompt">Select Sensor:</div>
        <div class="types">
            <label>
                <input type="radio" name="sensor" value="LD2450" />
                <div class="option-content">
                    <img src="images/ld2450.png" alt="LD2450" class="option-image">
                    <div>
                        <div class="title">LD2450</div>
                        <div class="description">The HiLink LD2450 supports 6m range, tracking of 3 targets and zones. This is the sensor that ships with the Everyting Presence Lite sensor.</div>
                        <a href="https://s.click.aliexpress.com/e/_DBh0oMt" target="_blank" rel="noopener noreferrer" class="purchase-link">Buy</a>
                    </div>
                </div>
            </label>
            <div id="advancedSensorsDivider" class="advanced-sensors-divider">Additional Sensors</div>
            <div id="advancedSensors" class="hidden">
                <label>
                    <input type="radio" name="sensor" value="DFRobot SEN0395" />
                    <div class="option-content">
                        <img src="images/sen0395.png" alt="DFRobot SEN0395" class="option-image">
                        <div>
                            <div class="title">DFRobot SEN0395</div>
                            <div class="description">The DFRobot SEN0395 has an 8m range, configurable distance, sensitivity and latency. It is extremely reliable for static presence detection and used in the <a href="https://shop.everythingsmart.io/products/everything-presence-one-kit" target="_blank" rel="noopener noreferrer">Everything Presence One</a>.</div>
                            <a href="https://www.dfrobot.com/product-2282.html?tracking=NKIPMR1X7YgIqIre4Lzs1ENvaBRhjQN1dac0FK9LO21raHxHPg5XMXWQ4pdTxdlH" target="_blank" rel="noopener noreferrer" class="purchase-link">Buy</a>
                        </div>
                    </div>
                </label>
                <label>
                    <input type="radio" name="sensor" value="SEN0609" />
                    <div class="option-content">
                        <img src="images/sen0609.png" alt="SEN0609" class="option-image">
                        <div>
                            <div class="title">SEN0609</div>
                            <div class="description">The new DFRobot SEN0609 has a 25m range, 2 configurable sensitvity levels and is extremely reliable at static presence. Select this option if you are using the DFRobot SEN0609 sensor (5 Pin).</div>
                            <a href="https://www.dfrobot.com/product-2793.html?tracking=NKIPMR1X7YgIqIre4Lzs1ENvaBRhjQN1dac0FK9LO21raHxHPg5XMXWQ4pdTxdlH" target="_blank" rel="noopener noreferrer" class="purchase-link">Buy</a>
                        </div>
                    </div>
                </label>
                <label>
                    <input type="radio" name="sensor" value="LD2410C" />
                    <div class="option-content">
                        <img src="images/ld2410c.png" alt="LD2410C" class="option-image">
                        <div>
                            <div class="title">LD2410C</div>
                            <div class="description">The HiLink LD2410 has a 6m range, supports configurable distance, sensitivity and a single target tracking for a very affordable price.</div>
                            <a href="https://s.click.aliexpress.com/e/_DmNyqWH" target="_blank" rel="noopener noreferrer" class="purchase-link">Buy</a>
                        </div>
                    </div>
                </label>
                <label>
                    <input type="radio" name="sensor" value="Seeed 24Ghz Lite" />
                    <div class="option-content">
                        <img src="images/seeed-mmwave-lite.png" alt="Seeed 24Ghz Lite" class="option-image">
                        <div>
                            <div class="title">Seeed 24Ghz Lite</div>
                            <div class="description">The Seeed 24Ghz Lite has a 5m range, supports configurable distance, sensitivity and a single target tracking for a very affordable price.</div>
                            <a href="https://www.seeedstudio.com/24GHz-mmWave-Sensor-Human-Static-Presence-Module-Lite-p-5524.html?sensecap_affiliate=TcBAarc&referring_service=link" target="_blank" rel="noopener noreferrer" class="purchase-link">Buy</a>
                        </div>
                    </div>
                </label>
            </div>
        </div>
    </div>

    <div id="homeAssistantOptions" class="hidden">
        <div class="question-prompt">Select firmware:</div>
        <div class="types">
            <label>
                <input type="radio" name="haOption" value="Bluetooth" />
                <div class="option-content">
                    <div class="title">Bluetooth Proxy</div>
                    <div class="description">Choose this option to enable Bluetooth Proxy and Improv. Can cause connectivity issues with WiFi.</div>
                </div>
            </label>
            <label>
                <input type="radio" name="haOption" value="No-Bluetooth" />
                <div class="option-content">
                    <div class="title">No Bluetooth</div>
                    <div class="description">Choose this option to disable Bluetooth Proxy and Improv, which can improve stability of the WiFi connection and/or you don't need Bluetooth Proxy.</div>
                </div>
            </label>
        </div>
    </div>
    <div id="summary" class="summary hidden">
        <h3>Your are flashing:</h3>
        <p id="summaryPlatform"></p>
        <p id="summarySensor"></p>
        <p id="summaryOption"></p>
    </div>
    <esp-web-install-button class="hidden"></esp-web-install-button>
</div>

## Next Steps

With the Lite fully updated and connected to WiFi, the final step is to connect it to Home Assistant.

[Connecting to Home Assistant](./Home%20Assistant/connecting-home-assistant.html){: .btn .btn-blue }

<script
    type="module"
    src="https://unpkg.com/esp-web-tools@9/dist/web/install-button.js?module"
></script>

<script>
const toggleDarkMode = document.querySelector('.js-toggle-dark-mode');

jtd.addEvent(toggleDarkMode, 'click', function(){
  if (jtd.getTheme() === 'dark') {
    jtd.setTheme('light');
    toggleDarkMode.textContent = 'Preview dark color scheme';
  } else {
    jtd.setTheme('light');
    toggleDarkMode.textContent = 'Return to the light side';
  }
});
</script>

<script>
document.addEventListener("DOMContentLoaded", function() {
    function clearSelectedOption(groupSelector) {
        document.querySelectorAll(groupSelector + ' label').forEach(label => {
            label.classList.remove('selected-option');
        });
    }

    function handleRadioButtonChange(event, groupSelector) {
        clearSelectedOption(groupSelector);
        event.target.closest('label').classList.add('selected-option');
    }

    document.querySelectorAll('input[name="platform"]').forEach(radio => {
        radio.addEventListener("change", function(event) {
            handleRadioButtonChange(event, '.types');
            
            var selectedPlatform = event.target.value;
            var sensorOptions = document.getElementById("sensorOptions");
            var homeAssistantOptions = document.getElementById("homeAssistantOptions");
            var installButton = document.querySelector("esp-web-install-button");

            sensorOptions.classList.add("hidden");
            homeAssistantOptions.classList.add("hidden");
            installButton.classList.add("hidden");

            if (selectedPlatform === "Home Assistant") {
                sensorOptions.classList.remove("hidden");
            }
        });
    });

    document.querySelectorAll('input[name="sensor"]').forEach(sensorRadio => {
        sensorRadio.addEventListener("change", function(event) {
            handleRadioButtonChange(event, '#sensorOptions .types');
            var homeAssistantOptions = document.getElementById("homeAssistantOptions");
            homeAssistantOptions.classList.remove("hidden");
        });
    });

    document.querySelectorAll('input[name="haOption"]').forEach(optionRadio => {
        optionRadio.addEventListener("change", function(event) {
            handleRadioButtonChange(event, '#homeAssistantOptions .types');

            var installButton = document.querySelector("esp-web-install-button");
            installButton.classList.remove("hidden");

            var selectedSensor = document.querySelector('input[name="sensor"]:checked').value;
            var selectedOption = this.value;
            var selectedPlatform = document.querySelector('input[name="platform"]:checked').value;

            document.getElementById("summaryPlatform").textContent = "Platform: " + selectedPlatform;
            document.getElementById("summarySensor").textContent = "Sensor: " + selectedSensor;
            document.getElementById("summaryOption").textContent = "Firmware: " + selectedOption;
            document.getElementById("summary").classList.remove("hidden");

            if (selectedSensor === "LD2450" && selectedOption === "Bluetooth") {
                installButton.setAttribute("manifest", "https://everythingsmarthome.github.io/everything-presence-lite/everything-presence-lite-ha-manifest.json");
            } else if (selectedSensor === "LD2450" && selectedOption === "No-Bluetooth") {
                installButton.setAttribute("manifest", "https://everythingsmarthome.github.io/everything-presence-lite/everything-presence-lite-ha-no-ble-manifest.json");
            } else if (selectedSensor === "LD2410C" && selectedOption === "Bluetooth") {
                installButton.setAttribute("manifest", "https://everythingsmarthome.github.io/everything-presence-lite/everything-presence-lite-ha-ld2410-manifest.json");
            } else if (selectedSensor === "LD2410C" && selectedOption === "No-Bluetooth") {
                installButton.setAttribute("manifest", "https://everythingsmarthome.github.io/everything-presence-lite/everything-presence-lite-ha-ld2410-no-ble-manifest.json");
            } else if (selectedSensor === "DFRobot SEN0395" && selectedOption === "Bluetooth") {
                installButton.setAttribute("manifest", "https://everythingsmarthome.github.io/everything-presence-lite/everything-presence-lite-ha-sen0395-manifest.json");
            } else if (selectedSensor === "DFRobot SEN0395" && selectedOption === "No-Bluetooth") {
                installButton.setAttribute("manifest", "https://everythingsmarthome.github.io/everything-presence-lite/everything-presence-lite-ha-sen0395-no-ble-manifest.json");
            } else if (selectedSensor === "Seeed 24Ghz Lite" && selectedOption === "Bluetooth") {
                installButton.setAttribute("manifest", "https://everythingsmarthome.github.io/everything-presence-lite/everything-presence-lite-ha-mr24hpc1-manifest.json");
            } else if (selectedSensor === "Seeed 24Ghz Lite" && selectedOption === "No-Bluetooth") {
                installButton.setAttribute("manifest", "https://everythingsmarthome.github.io/everything-presence-lite/everything-presence-lite-ha-mr24hpc1-no-ble-manifest.json");
            } else if (selectedSensor === "SEN0609" && selectedOption === "Bluetooth") {
                installButton.setAttribute("manifest", "https://everythingsmarthome.github.io/everything-presence-lite/everything-presence-lite-ha-sen0609-manifest.json");
            } else if (selectedSensor === "SEN0609" && selectedOption === "No-Bluetooth") {
                installButton.setAttribute("manifest", "https://everythingsmarthome.github.io/everything-presence-lite/everything-presence-lite-ha-sen0609-no-ble-manifest.json");
            }
        });
    });
});

document.getElementById("advancedSensorsDivider").addEventListener("click", function() {
    var advancedSensors = document.getElementById("advancedSensors");
    advancedSensors.classList.toggle("hidden");
});
</script>
