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
  <img src="/Aqua-Sense%20BLE/images/Aqua-Sense%20BLE_1.jpg" width="300">
  <br/>
  <sub>Разбудите сенсор нажатием кнопки или замыканием контактов</sub>
</div>

### Шаг 4: Найти устройство в приложении

В приложении найдите устройство с именем:

<div align="center">
  <img src="/Aqua-Sense%20BLE/images/Aqua-Sense%20BLE_3.jpg" width="300">
  <br/>
  <sub>Имя устройства: <strong>LD-S</strong></sub>
</div>

### Шаг 5: Записать MAC-адрес

Запишите MAC-адрес найденного устройства — он понадобится для настройки в ESPHome.

---

## 🏠 Интеграция с Home Assistant

Для полноценной работы датчика в системе **Home Assistant** разработана специальная интеграция.

### ✨ Возможности интеграции

| Функция | Описание |
|---------|----------|
| 📊 **Батарея** | Отображение уровня заряда в процентах |
| 💧 **Протечка** | Детекция воды на корпусе датчика |
| 🔌 **Внешний датчик** | Сработка от внешнего проводного датчика |
| 🔘 **Кнопка** | Распознавание нажатий (короткое, долгое, очень долгое) |
| 📡 **События** | Генерация событий для автоматизаций |

### 📥 Установка интеграции

Интеграция устанавливается через **HACS** (Home Assistant Community Store):

1. Добавьте пользовательский репозиторий:  
   `https://github.com/NagibinA/ha-ujin-aqua-sense`
2. Категория: **Интеграция**
3. Установите интеграцию **Ujin Aqua-Sense BLE**
4. Перезапустите Home Assistant

### 🔧 Настройка

1. **Настройки** → **Устройства и сервисы** → **Добавить интеграцию**
2. Найдите **"Ujin Aqua-Sense BLE"**
3. Введите MAC-адрес вашего датчика (например: `01:00:5E:00:38:C8`)

### 📊 Сущности в Home Assistant

После настройки появятся следующие сущности:

| Тип | Название | Описание |
|-----|----------|----------|
| Сенсор | `sensor.ujin_aqua_sense_battery` | Уровень заряда батареи (0-100%) |
| Бинарный сенсор | `binary_sensor.ujin_aqua_sense_protechka` | Встроенный датчик протечки |
| Бинарный сенсор | `binary_sensor.ujin_aqua_sense_vneshniy_datchik` | Внешний датчик протечки |
| Бинарный сенсор | `binary_sensor.ujin_aqua_sense_knopka_nazhatie` | Нажатие кнопки |

### 📋 События для автоматизаций

| Событие | Описание |
|---------|----------|
| `ujin_aqua_sense_leak` | Обнаружена протечка на корпусе |
| `ujin_aqua_sense_input_leak` | Сработал внешний датчик |
| `ujin_aqua_sense_button` | Нажата кнопка (тип: `press`/`long_press`/`very_long_press`) |

### 🔗 Ссылки

- **Репозиторий интеграции:** [NagibinA/ha-ujin-aqua-sense](https://github.com/NagibinA/ha-ujin-aqua-sense)
- **Установка через HACS:** Пользовательский репозиторий `NagibinA/ha-ujin-aqua-sense`
- **Автор интеграции:** [NagibinA](https://github.com/NagibinA)

---

### Информация по разбору передаваемых байтов в пакете

**Пример пакета (HEX):**

05 09 4C 44 2D 53 08 FF FF FF 03 07 50 04 73


#### Имя устройства

| Блок | Байт  | Значение |
|------|------|----------|
| Длина блока |(0x05) | 5 |
| Тип | 0x09 | (маркер что далее имя) |
| Имя |(4C 44 2D 53)  |LD-S  |

✅ **Имя устройства: LD-S**

#### Основной блок данных (8 байт)

| Блок | Байт  |Значение |
|------|------|----------|
| Длина блока | 0x08 |8 |
| Тип | 0xFF |  (маркер что далее Manufacturer ID) |
| Manufacturer ID | 0xFFFF | FFFF |
| initial | 0x0307  | (1795) всегда фиксирован |
| battery | 0x50  | (80%) |
| status | 0x04 |status = 0x04 (бит 2 = input) |
| counter | 0x73  |(115) |


#### Таблица статусов (байт 0x04)

| Событие | Бит | Десятичное | Двоичное | HEX |
|---------|-----|------------|----------|-----|
| very long press | 6 | 64 | 0b01000000 | 0x40 |
| long press | 5 | 32 | 0b00100000 | 0x20 |
| **input** | **2** | **4** | **0b00000100** | **0x04** ← ТЕКУЩИЙ |
| leak | 1 | 2 | 0b00000010 | 0x02 |
| press button | 0 | 1 | 0b00000001 | 0x01 |

---

**📊 ИТОГ:** LD-S | 🔋 80% | 🖱️ input 

---


#### Пример отображения датчиков в прошивке

<div align="center">
  <img src="/Aqua-Sense%20BLE/images/Aqua-Sense%20BLE_4.png" width="500">
  <br/>
  <sub></sub>
</div>
