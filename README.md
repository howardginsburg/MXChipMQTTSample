# MXChip Sending Sensor Data via MQTT

This project represents a simple example of sending sensor data from an [MXChip (AZ3166)](https://microsoft.github.io/azure-iot-developer-kit/) device to a standard MQTT broker using the updated [sdk](https://github.com/howardginsburg/framework-arduinostm32mxchip).  The MXChip device is a development board that includes a variety of sensors and can be programmed using [PlatformIO](https://platformio.org/). The device is connected to the network via Wi-Fi and sends sensor data to a MQTT broker.  Note, this sample does not support TLS, so it is not secure.  

## Prerequisites

1. [MXChip (AZ3166)](https://microsoft.github.io/azure-iot-developer-kit/)
1. [PlatformIO](https://platformio.org/) installed in [Visual Studio Code](https://code.visualstudio.com/)

## MXChip Device Setup

### Option 1: Using the PlatformIO IDE

1. Clone this repository to your local machine.
1. Open Visual Studio Code to the project directory.
1. Optionally, update the `platformio.ini` file with if you want to override some of the default settings used in the code.
1. Build and upload the project to the MXChip device.

### Option 2: Copy the compiled binary to the MXChip device

1. Download the [binary](/binary/mxchip_mqttsample.bin) file and copy it to your MXChip device.

## Device Configuration

1. Plug the MXChip device into your computer using a USB cable.
1. As it boots, press and hold the A button to enter the configuration mode.
1. Configure the wifi, mqtt broker, and other settings as needed.

### Understanding the flashing lights!

1. When the device connects to Wifi, the small green LED will turn on.
1. As the device reads data, the large LED will flash to indicate:
   - Green: Successfully sent data to the MQTT broker
   - Blue: Data has not changed enough to send to the MQTT broker
   - Red: Failed to send data to the MQTT broker.