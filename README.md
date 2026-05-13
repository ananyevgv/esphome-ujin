[![License][license-shield]][license]
[![ESPHome release][esphome-release-shield]][esphome-release]

[license-shield]: https://img.shields.io/static/v1?label=License&message=MIT&color=orange&logo=license
[license]: https://opensource.org/licenses/MIT
[esphome-release-shield]: https://img.shields.io/static/v1?label=ESPHome&message=2026.4&color=green&logo=esphome
[esphome-release]: https://GitHub.com/esphome/esphome/releases/

<div align="center">
  <h1>⚡ Устройства UJIN в ESPHome</h1>
  <p><strong>Готовые конфигурации, даташиты и прошивки для умного дома</strong></p>
  <br/>
</div>

> ⚠️ **Важно**: Перед прошивкой на ESPHome обязательно посмотрите LOG устройства и сделайте **резервную копию (backup)**.

---

## 🧩 Поддерживаемые устройства

### 💡 Освещение и свет
| Lume Luxe L.te M1 | Lume Wi-Fi Z1 | Lume Luxe L.te M2 | Ujin EKF |
|:---:|:---:|:---:|:---:|
| [![Lume Luxe L.te M1](/Lume%20Luxe_L.te%20M1/images/Luxe_Lte%20M1_1.jpg)](/Lume%20Luxe_L.te%20M1) | [![Lume Wi-Fi Z1](/Lume%20Wi-Fi_Z1/images/Lume%20WIFI%20Z1.jpg)](/Lume%20Wi-Fi_Z1) | [![Lume Luxe L.te M2](/Lume%20Luxe_L.te%20M2/images/Lume%20Luxe_L.te%20M2.jpg)](/Lume%20Luxe_L.te%20M2) | [![Pulse_EP_WBZ_T_MNI](/Pulse_EP_WBZ_T_MNI/images/Pulse_EP_WBZ_T_MNI_1.jpg)](/Pulse_EP_WBZ_T_MNI) |

| Lume Wi-Fi + BLE/IR/CO₂ | Lume LED | lume‑in |
|:---:|:---:|:---:|
| [![wifi/BLE/IR/CO2](/Lume%20Wi-Fi_BLE_IR_CO2/images/Lume%20wifi_BLE_IR_CO2_1.jpg)](/Lume%20Wi-Fi_BLE_IR_CO2) | [![Lume LED](/led/images/lume-led.jpg)](/led) | [![lume-in](/lume-in/images/lume-in.jpg)](/lume-in) |

### 💧 Вода и защита от протечек
| Aqua Sense (BLE) | Aqua Wi-Fi (220В) | Aqua EKF | Drive |
|:---:|:---:|:---:|:---:|
| [![Aqua Sense](/Aqua-Sense%20BLE/images/Aqua-Sense%20BLE.jpg)](/Aqua-Sense%20BLE) | [![Aqua Wi-Fi](/Aqua%20Wi-Fi_BLE_220%D0%92_%D0%A1%D0%A3-02_R2/images/Aqua%20Wi-Fi_1.jpg)](/Aqua%20Wi-Fi_BLE_220%D0%92_%D0%A1%D0%A3-02_R2) | [![Aqua EKF](/Aqua-EA/images/ujin-ekf-aqua.jpg)](/Aqua-EA) | [![Drive](/drive/images/driveS.jpg)](/drive) |

для проводного датчика UAS-W подержка в пакете valve

### 🌡️Термостаты
| Heat Wi-Fi | Heat EKF |
|:---:|:---:|
| [![Heat Wi-Fi](/Heat%20Wi-Fi/images/heat_1.jpg)](/Heat%20Wi-Fi) | [![Heat](/Heat/images/heat.jpg)](/Heat) |

### 🎛️ Коммутаторы реле
| Connect din Wi-Fi | Connect‑in |
|:---:|:---:|
| [![Connect din](/Connect-din%20Wi-Fi/images/connect-din_wi-fi.jpg)](/Connect-din%20Wi-Fi) | [![Connect-in](/connect-in/images/connect_in0.jpg)](/connect-in) |

---

## 📖 Полезная информация

| 📄 Документация | 🔗 Ссылка |
|----------------|-----------|
| 🧠 Расшифровка моделей по датчикам | [`/datasheet/data.jpg`](/datasheet/data.jpg) |
| 📚 Даташиты на компоненты | [`/datasheet`](./datasheet) |
| ⚠️ Отличие устройств Pulse | Отсутствие исполнительных устройств ( таких как диммер, реле) |
| 🎛️ Connect din Wi-Fi | Коммутатор с двумя реле на DIN-рейку |
| 🔌 Connect‑in | Реле в подрозетник |
| 🎚️ lume‑in | Диммер в подрозетник |

---

## 🛠️ Проекты с использованием UJIN

| Проект | Описание |
|--------|----------|
| [❄️ «Зимняя вода для улицы»](/drive/winter_water) | Защита системы водоснабжения в морозы |
| [🔄 Альтернативная плата под корпус EKF](/board/) | Замена платы для Aqua, Pulse, Heat (корпус EKF) |

---

<div align="center">
  <sub>
    📦 ESPHome 2026.4+
  </sub>
</div>
