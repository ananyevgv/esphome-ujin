[![License][license-shield]][license]
[![ESPHome release][esphome-release-shield]][esphome-release]

[license-shield]: https://img.shields.io/static/v1?label=License&message=MIT&color=orange&logo=license
[license]: https://opensource.org/licenses/MIT
[esphome-release-shield]: https://img.shields.io/static/v1?label=ESPHome&message=2026.4&color=green&logo=esphome
[esphome-release]: https://GitHub.com/esphome/esphome/releases/

<div align="center">
  <h1>💧 UAS-B  — Датчик протечки воды</h1>
  <p><strong>Беспроводной сенсор протечки с псевдо-BLE на чипе NRF24</strong></p>
  <br/>
</div>


---

## 📌 Совместимость

| Модель | Тип | Поддержка |
|--------|-----|-----------|
| **UAS-B** | Беспроводной | ✅ через псевдо-BLE (NRF24) |


---

## 🔧 Технические особенности

| Параметр | Описание |
|----------|----------|
| **Чип** | NRF24 (эмулирует псевдо-BLE) |
| **Протокол** | BLE-совместимый (нестандартный) |
| **Питание** | Автономное (батарейное) |

---

## 📍 Пошаговая настройка подключения к ESPHome

### Шаг 1: Узнать MAC-адрес сенсора

Для подключения датчика к ESPHome необходимо узнать его **MAC-адрес**.

### Шаг 2: Скачать приложение для сканирования BLE

Воспользуйтесь любым приложением для сканирования Bluetooth LE, например:

📱 **Bluetooth LE Scanner** (доступно для iOS и Android)

### Шаг 3: Разбудить сенсор

<div align="center">
  <img src="/Aqua-Sense%20BLE/images/Aqua-Sense%20BLE_3.jpg" width="300">
  <br/>
  <sub>Разбудите сенсор нажатием кнопки или замыканием контактов</sub>
</div>

### Шаг 4: Найти устройство в приложении

В приложении найдите устройство с именем:

<div align="center">
  <img src="/Aqua-Sense%20BLE/images/Aqua-Sense%20BLE_3.png" width="300">
  <br/>
  <sub>Имя устройства: <strong>LD-S</strong></sub>
</div>

### Шаг 5: Записать MAC-адрес

Запишите MAC-адрес найденного устройства — он понадобится для настройки в ESPHome.

---

