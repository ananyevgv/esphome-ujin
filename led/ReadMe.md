[![License][license-shield]][license]
[![ESPHome release][esphome-release-shield]][esphome-release]

[license-shield]: https://img.shields.io/static/v1?label=License&message=MIT&color=orange&logo=license
[license]: https://opensource.org/licenses/MIT
[esphome-release-shield]: https://img.shields.io/static/v1?label=ESPHome&message=2026.4&color=green&logo=esphome
[esphome-release]: https://GitHub.com/esphome/esphome/releases/

<div align="center">
  <h1>⚡ ULL-WB-5C-M</h1>
  <p><strong>5-канальный MOSFET-контроллер с контролем тока и напряжения</strong></p>
  <br/>
</div>

> ⚠️ **Важно**: Перед прошивкой на ESPHome обязательно посмотрите LOG устройства и сделайте **резервную копию (backup)**.

---

## 📌 Информация об устройстве

| Параметр | Значение |
|----------|----------|
| **MCU** | ESP32-PICO-V3-02 |
| **Модель** | ujin-pt-led-din-ch-m2 |

---

## 🧩 Аппаратная комплектация

| Компонент | Количество / Описание |
|-----------|----------------------|
| MOSFET | **5 шт.** (TPN2R703NL) с контролем тока и напряжения |
| Входы | **2 шт.** |
| Светодиоды (LED) | **2 шт.** |
| Кнопка | **1 шт.** |
| Датчик температуры | RK1 NTC |

---

## 🔧 Особенности

| Функция | Описание |
|---------|----------|
| 🔌 Контроль тока | ✅ — на каждом MOSFET-канале |
| ⚡ Контроль напряжения | ✅ |
| 🌡️ Датчик температуры | NTC-термистор |
| 🎮 Кнопка | Тактильная, для управления/сброса |

---

## 📊 Краткая спецификация

| Параметр | Значение |
|----------|----------|
| MCU | ESP32-PICO-V3-02 |
| Силовые ключи | 5 × TPN2R703NL |
| Контроль тока | ✅ |
| Контроль напряжения | ✅ |
| Входы | 2 |
| LED-индикаторы | 2 |
| Кнопка | 1 |
| Датчик температуры | RK1 NTC |

---

## 💡 Применение

Устройство предназначено для:

- Управления несколькими нагрузками с независимым контролем тока и напряжения
- Систем автоматизации, где требуется мониторинг потребляемой мощности

---

<div align="center">
  <sub>
    💡 Разработано для ESPHome | 
    📦 Требуется ESPHome 2026.4+
  </sub>
</div>