[![License][license-shield]][license]
[![ESPHome release][esphome-release-shield]][esphome-release]

[license-shield]: https://img.shields.io/static/v1?label=License&message=MIT&color=orange&logo=license
[license]: https://opensource.org/licenses/MIT
[esphome-release-shield]: https://img.shields.io/github/v/release/esphome/esphome?label=ESPHome&color=green&logo=esphome
[esphome-release]: https://GitHub.com/esphome/esphome/releases/

<div align="center">
  <h1>⚡ Устройства UJIN в ESPHome</h1>
  <p><strong>Готовые конфигурации, даташиты и прошивки для умного дома</strong></p>
  <br/>
</div>

> ⚠️ **Важно**: Перед прошивкой на ESPHome обязательно посмотрите LOG устройства и сделайте **резервную копию (backup)**.

---

## 🧩 Поддерживаемые устройства

### 💡 Выключатели
| Lume Luxe L.te M1 | Lume Wi-Fi Z1 | Lume Luxe L.te M2 | Ujin EKF |
|:---:|:---:|:---:|:---:|
| [<img src="/Lume%20Luxe_L.te%20M1/images/Luxe_Lte%20M1_1.jpg" width="250">](/Lume%20Luxe_L.te%20M1) | [<img src="/Lume%20Wi-Fi_Z1/images/Lume%20WIFI%20Z1.jpg" width="250">](/Lume%20Wi-Fi_Z1) | [<img src="/Lume%20Luxe_L.te%20M2/images/Lume%20Luxe_L.te%20M2.jpg" width="250">](/Lume%20Luxe_L.te%20M2) | [<img src="/Pulse_EP_WBZ_T_MNI/images/Pulse_EP_WBZ_T_MNI_1.jpg" width="250">](/Pulse_EP_WBZ_T_MNI) |

| Lume Wi-Fi + BLE/IR/CO₂ | 
|:---:|
| [<img src="/Lume%20Wi-Fi_BLE_IR_CO2/images/Lume%20wifi_BLE_IR_CO2_1.jpg" width="250" alt="Lume Wi-Fi BLE IR CO2">](/Lume%20Wi-Fi_BLE_IR_CO2) |

 ⚠️ Отличие устройств Pulse - отсутствие исполнительных устройств ( таких как диммер, реле) 

### 💧 Вода и защита от протечек
| Aqua Sense (BLE) | Aqua Wi-Fi | Aqua EKF | Drive |
|:---:|:---:|:---:|:---:|
| [<img src="/Aqua-Sense%20BLE/images/Aqua-Sense%20BLE.jpg" width="250" alt="Aqua Sense">](/Aqua-Sense%20BLE) | [<img src="/Aqua%20Wi-Fi_BLE_220%D0%92_%D0%A1%D0%A3-02_R2/images/Aqua%20Wi-Fi_1.jpg" width="250" alt="Aqua Wi-Fi">](/Aqua%20Wi-Fi_BLE_220%D0%92_%D0%A1%D0%A3-02_R2) | [<img src="/Aqua-EA/images/ujin-ekf-aqua.jpg" width="250" alt="Aqua EKF">](/Aqua-EA) | [<img src="/drive/images/driveS.jpg" width="250" alt="Drive">](/drive) |

для проводного датчика UAS-W подержка в пакете valve

### 🌡️Термостаты
| Heat Wi-Fi | Heat EKF |
|:---:|:---:|
| [<img src="/Heat%20Wi-Fi/images/heat_1.jpg" width="250" alt="Heat Wi-Fi">](/Heat%20Wi-Fi) | [<img src="/Heat/images/heat.jpg" width="250" alt="Heat">](/Heat) |

### 🎛️ Прочее
| Connect din Wi-Fi | Connect‑in | Lume LED | lume‑in |
|:---:|:---:|:---:|:---:|
| [<img src="/Connect-din%20Wi-Fi/images/connect-din_wi-fi.jpg" width="250" alt="Connect din">](/Connect-din%20Wi-Fi) | [<img src="/connect-in/images/connect_in0.jpg" width="250" alt="Connect-in">](/connect-in) | [<img src="/led/images/lume-led.jpg" width="250" alt="Lume LED">](/led) | [<img src="/lume-in/images/lume-in.jpg" width="250" alt="lume-in">](/lume-in) |
| 🎛️ Коммутатор с двумя реле на DIN-рейку | 🔌 Реле в подрозетник | 🎚️ 5 канальный контроллер LED ленты | 🎚️ Диммер в подрозетник |

---

## 📖 Полезная информация

| 📄 Документация | 🔗 Ссылка |
|----------------|-----------|
| 🧠 Расшифровка моделей по датчикам | [`/datasheet/data.jpg`](/datasheet/data.jpg) |
| 📚 Даташиты на компоненты | [`/datasheet`](./datasheet) |

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

## ⭐ Поддержать проект

Если проект оказался полезным — поставьте ⭐ на GitHub!
