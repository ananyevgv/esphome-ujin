# 🔧 Flashing Guide for EH-WB Thermostat (ESP32) via UART

Step-by-step guide to backing up the factory firmware and flashing ESPHome,
taking into account all the nuances from the documentation of the
[`ananyevgv/esphome-ujin`](https://github.com/ananyevgv/esphome-ujin/tree/main/Heat) project.

---

## ⚠️ Step 0: Important warnings from the ReadMe

Before you start, be sure to consider two things:

1. **Make a backup** — the ReadMe states:
   > "Before flashing ESPHome, be sure to check the device LOG and make a backup."

2. **3.3V power** — the ReadMe states:
   > "Some boards do not have a 3.3V linear regulator — it is installed in the mating part. When flashing, 3.3V must be supplied, or the mating part must be connected."

   This means your USB-UART programmer must output **3.3V**, and you must supply this power to the board.

---

## 📥 Step 1: Reading the factory firmware (backup)

This is a critical step so that you can restore the device to its original state if needed.

1. **Connect the USB-UART programmer** to the ESP32 pins on the thermostat board:

   | Programmer | Thermostat board |
   | :--- | :--- |
   | GND | GND |
   | TX | RX (usually `GPIO3`) |
   | RX | TX (usually `GPIO1`) |
   | 3.3V | 3.3V |

2. **Put the ESP32 into bootloader mode**: hold the **BOOT** button (or short `GPIO0` to GND) and briefly press **RESET**.

3. **Read the dump** using `esptool.py`. For the ESP32-PICO-V3-02 with 8 MB of flash (the standard size for this model), the command is:

   ```bash
   esptool.py --port COM4 read_flash 0x0 0x800000 factory_backup.bin
   ```

   * Replace `COM4` with your port.
   * `0x800000` is 8 MB. If you have 4 MB, use `0x400000`.

---

## 📝 Step 2: Preparing the ESPHome configuration

1. **Download the project files**: go to the [`Heat`](https://github.com/ananyevgv/esphome-ujin/tree/main/Heat) folder in the `ananyevgv/esphome-ujin` repository and download the main YAML file (e.g. `heat.yaml`).

2. **Create a device in ESPHome**: in Home Assistant, open the ESPHome dashboard, click **NEW DEVICE**, create an empty device and name it (e.g. `ujin-heat`).

3. **Paste the configuration**: open the downloaded YAML file from the repository and copy its contents into the ESPHome editor, replacing the generated code.

4. **Configure `secrets.yaml`**: make sure your `secrets.yaml` file (in the `/config/esphome/` folder) contains the correct Wi-Fi credentials. If not, add:

   ```yaml
   wifi_ssid: "Your_SSID"
   wifi_password: "Your_password"
   ```

> **Note:** the ReadMe states that **ESPHome 2026.4+** is required, so make sure your add-on is up to date.

---

## ⚡ Step 3: Flashing the device

Now you can write your own firmware.

### Option A: Via the ESPHome web interface (recommended)

1. In the ESPHome dashboard, on your device card (`ujin-heat`), click **INSTALL**.
2. Choose **Plug into the computer running ESPHome Dashboard**.
3. From the drop-down list, select the COM port of your USB-UART programmer.
4. Click **INSTALL**. ESPHome will compile the firmware and flash it to the device.

### Option B: Via the command line

If you prefer the CLI, you can use `esphome run`, which compiles and flashes in one step:

```bash
esphome run heat.yaml --device COM4
```

* Replace `heat.yaml` with your file name, and `COM4` with your port.

### If flashing fails

* **Lower the speed**: some USB-UART adapters (CH340, CP2102) are unstable at high speeds. Try lowering the speed in the YAML file by adding:

  ```yaml
  upload_speed: 115200
  ```

* **Check the power**: double-check that **3.3V** is supplied to the board, as stated in the ReadMe.

---

## ✅ Step 4: After flashing

1. Disconnect the programmer from the board.
2. Press the **RESET** button on the device (or power-cycle it).
3. The device should connect to your Wi-Fi network and be automatically discovered in Home Assistant via the ESPHome integration.
4. All future updates can be done **over the air (OTA)** — no wires needed.
