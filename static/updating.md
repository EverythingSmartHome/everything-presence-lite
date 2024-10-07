---
layout: default
title: Updating and Connecting to WiFi
nav_order: 4
---

# Updating and Connecting To WiFi

{: .no_toc }

This page will help you to flash and update your Everything Presence Lite to the latest version and get it connected to WiFi!
{: .fs-6 .fw-300 }

## Automatic Setup

If you have the new Everything Presence Lite that comes fully assembled with the injection moulded case, your device comes pre-installed from the factory ready to go. You can benefit from automatic setup in Home Assistant, if your Home Assistant server has [bluetooth enabled](https://www.home-assistant.io/integrations/bluetooth/).

If you have Bluetooth enabled, as soon as you power the Everything Presence Lite, Home Assistant should automagically discover it on the Device page:

![Home Assistant BLE Improv setup](images/home-assistant-ble-improv-setup.png)

Follow the prompts, entering your WiFi details to get the Lite connected to your home network.

![Home Assistant BLE Improv setup](images/home-assistant-ble-improv-setup-wifi.png)

## Next Steps

Once connected to WiFi, you are ready to connect to Home Assistant.

[Connecting to Home Assistant](./Home%20Assistant/connecting-home-assistant.html){: .btn .btn-blue }

## Manual Setup and Factory Resetting

The steps below are for the following users:

- You have the Everything Presence Lite Kit with the 3D printed case
- You don't have Bluetooth enabled in Home Assistant and can't do the automatic setup above
- You want to factory reset the firmware and start again

This process below will guide you through installing the latest firmware on your device, and get you connected to WiFi.

Here you can install the latest firmware on the Everything Presence Lite board for direct integration with [Home Assistant](https://home-assistant.io)

First, make sure you have the Lite connected to a USB port on your computer and select the platform you would like to install below. Hit the connect button, select the USB port from the list and then hit the install button to begin installing the latest software on your Everything Presence Lite.

Once the install has completed, you can then connect the Lite to your WiFi easily and securely.

{: .warning-title }
If you do not see a "Connect" button below, use a supported web browser like Google Chrome.

{: .warning-title }
After clicking the "Connect" button, if you do not see a "USB Serial" port listed, or you get the error "Failed to open serial port.", you may need to install the CH340 driver. The installer should give you links to the latest driver.

<div class="container">
    <div class="question-prompt">Select Smart Home Platform:</div>
    <div class="types platform-types">
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
        <div class="types sensor-types">
            <label>
                <input type="radio" name="sensor" value="LD2450" />
                <div class="option-content">
                    <img src="images/ld2450.png" alt="LD2450" class="option-image">
                    <div>
                        <div class="title">LD2450</div>
                        <div class="description">The HiLink LD2450 supports 6m range, tracking of 3 targets and zones. This is the sensor that ships with the Everything Presence Lite sensor.</div>
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
                            <div class="description">The new DFRobot SEN0609 has a 25m range, 2 configurable sensitivity levels and is extremely reliable at static presence. Select this option if you are using the DFRobot SEN0609 sensor (5 Pin).</div>
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

    <div id="moduleOptions" class="hidden">
        <div class="question-prompt">Select Module:</div>
        <div class="types module-types">
            <label>
                <input type="radio" name="module" value="No Module" />
                <div class="option-content">
                    <div class="title">No Module</div>
                    <div class="description">No additional module installed.</div>
                </div>
            </label>
            <label>
                <input type="radio" name="module" value="CO2 Module" />
                <div class="option-content">
                        <div class="title">CO2 Module</div>
                        <div class="description">Add support for the <a href="https://shop.everythingsmart.io/products/everything-presence-one-lite-co2-add-on">optional CO2 module</a>.</div>
                </div>
            </label>
        </div>
    </div>

    <div id="homeAssistantOptions" class="hidden">
        <div class="question-prompt">Select firmware:</div>
        <div class="types firmware-types">
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
        <h3>You are flashing:</h3>
        <p id="summaryPlatform"></p>
        <p id="summarySensor"></p>
        <p id="summaryModule"></p>
        <p id="summaryOption"></p>
    </div>
    <esp-web-install-button class="hidden"></esp-web-install-button>
</div>

## Next Steps

With the Lite fully updated and connected to WiFi, the final step is to connect it to Home Assistant.

[Connecting to Home Assistant](./Home%20Assistant/connecting-home-assistant.html){: .btn .btn-blue }

<script
    type="module"
    src="https://unpkg.com/esp-web-tools@10/dist/web/install-button.js?module"
></script>

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
            handleRadioButtonChange(event, '.platform-types');

            var selectedPlatform = event.target.value;
            var sensorOptions = document.getElementById("sensorOptions");
            var moduleOptions = document.getElementById("moduleOptions");
            var homeAssistantOptions = document.getElementById("homeAssistantOptions");
            var installButton = document.querySelector("esp-web-install-button");

            sensorOptions.classList.add("hidden");
            moduleOptions.classList.add("hidden");
            homeAssistantOptions.classList.add("hidden");
            installButton.classList.add("hidden");
            document.getElementById("summary").classList.add("hidden");

            clearSelectedOption('.sensor-types');
            clearSelectedOption('.module-types');
            clearSelectedOption('.firmware-types');

            if (selectedPlatform === "Home Assistant") {
                sensorOptions.classList.remove("hidden");
            }
        });
    });

    document.querySelectorAll('input[name="sensor"]').forEach(sensorRadio => {
        sensorRadio.addEventListener("change", function(event) {
            handleRadioButtonChange(event, '.sensor-types');
            var moduleOptions = document.getElementById("moduleOptions");
            moduleOptions.classList.remove("hidden");

            var homeAssistantOptions = document.getElementById("homeAssistantOptions");
            homeAssistantOptions.classList.add("hidden");
            var installButton = document.querySelector("esp-web-install-button");
            installButton.classList.add("hidden");
            document.getElementById("summary").classList.add("hidden");

            clearSelectedOption('.module-types');
            clearSelectedOption('.firmware-types');
        });
    });

    document.querySelectorAll('input[name="module"]').forEach(moduleRadio => {
        moduleRadio.addEventListener("change", function(event) {
            handleRadioButtonChange(event, '.module-types');
            var homeAssistantOptions = document.getElementById("homeAssistantOptions");
            homeAssistantOptions.classList.remove("hidden");

            var installButton = document.querySelector("esp-web-install-button");
            installButton.classList.add("hidden");
            document.getElementById("summary").classList.add("hidden");

            clearSelectedOption('.firmware-types');
        });
    });

    document.querySelectorAll('input[name="haOption"]').forEach(optionRadio => {
        optionRadio.addEventListener("change", function(event) {
            handleRadioButtonChange(event, '.firmware-types');

            var installButton = document.querySelector("esp-web-install-button");
            installButton.classList.remove("hidden");

            var selectedSensor = document.querySelector('input[name="sensor"]:checked').value;
            var selectedOption = this.value;
            var selectedPlatform = document.querySelector('input[name="platform"]:checked').value;
            var selectedModule = document.querySelector('input[name="module"]:checked').value;

            document.getElementById("summaryPlatform").textContent = "Platform: " + selectedPlatform;
            document.getElementById("summarySensor").textContent = "Sensor: " + selectedSensor;
            document.getElementById("summaryModule").textContent = "Module: " + selectedModule;
            document.getElementById("summaryOption").textContent = "Firmware: " + selectedOption;
            document.getElementById("summary").classList.remove("hidden");

            var sensorSuffix = "";
            if (selectedSensor === "LD2410C") {
                sensorSuffix = "-ld2410";
            } else if (selectedSensor === "DFRobot SEN0395") {
                sensorSuffix = "-sen0395";
            } else if (selectedSensor === "Seeed 24Ghz Lite") {
                sensorSuffix = "-mr24hpc1";
            } else if (selectedSensor === "SEN0609") {
                sensorSuffix = "-sen0609";
            }

            var optionSuffix = "";
            if (selectedOption === "No-Bluetooth") {
                optionSuffix = "-no-ble";
            }

            var moduleSuffix = "";
            if (selectedModule === "CO2 Module") {
                moduleSuffix = "-co2";
            }

            var manifestFilename = "everything-presence-lite-ha" + sensorSuffix + optionSuffix + moduleSuffix + "-manifest.json";

            var manifestURL = "https://everythingsmarthome.github.io/everything-presence-lite/" + manifestFilename;

            installButton.setAttribute("manifest", manifestURL);
        });
    });
});

document.getElementById("advancedSensorsDivider").addEventListener("click", function() {
    var advancedSensors = document.getElementById("advancedSensors");
    advancedSensors.classList.toggle("hidden");
});
</script>