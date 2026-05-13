[![License][license-shield]][license]
[![ESPHome release][esphome-release-shield]][esphome-release]

[license-shield]: https://img.shields.io/static/v1?label=License&message=MIT&color=orange&logo=license
[license]: https://opensource.org/licenses/MIT
[esphome-release-shield]: https://img.shields.io/static/v1?label=ESPHome&message=2026.4&color=green&logo=esphome
[esphome-release]: https://GitHub.com/esphome/esphome/releases/

<div align="center">
  <h1>📡 Connect-Din Wi-Fi</h1>
  <p><strong>Коммутатор на DIN-рейку </strong></p>
  <br/>
</div>

> ⚠️ **Важно**: Перед прошивкой на ESPHome обязательно посмотрите LOG устройства и сделайте **резервную копию (backup)**.

---

## 📌 Об устройстве

<div align="center">
  <img src="/Connect-din%20Wi-Fi/images/connect din.png" width="400">
  <br/>
  <sub>Внешний вид Connect-Din Wi-Fi</sub>
</div>
 <br/>

**Connect-Din Wi-Fi** — это коммутатор для управления электрическими нагрузками по двум каналам с помощью двух независимых электромагнитных реле с перекидными контактами. Коммутатор имеет два входа для подключения внешних выключателей, переключателей или проводных датчиков.

<div align="center">
  <img src="/Connect-din%20Wi-Fi/images/connect-din_wi-fi_5.png" width="400">
  <br/>
  <sub>Реализовано в прошивке</sub>
</div>
 <br/>

---

## 🔧 Способы прошивки

### Способ 1. Переход в режим прошивки через кнопку

Для перевода ESP в режим прошивки:

1. Нажмите и **удерживайте** кнопку **«Настройка»**
2. **Не отпуская** кнопку, подайте питание
3. Отпустите кнопку после подачи питания

<div align="center">
  <img src="/Connect-din%20Wi-Fi/images/connect din 0.png" width="400">
  <br/>
  <sub>Местоположение кнопки «Настройка» и пинов для подключения программатора</sub>
</div>

---

### Способ 2. Прошивка программатором CH341A с прищепкой

<div align="center">
  <img src="/Connect-din%20Wi-Fi/images/connect-din_wi-fi_firmware.jpg" width="400">
  <br/>
  <sub>Подключение прищепки к контактам флеш памяти для прошивки</sub>
</div>

<br/>

Для опытных пользователей — подробная инструкция:

🔗 [Прошивка BIOS программатором CH341A с прищепкой](http://xeonlive.ru/instruktsii/proshivka-bios-programmatorom-ch341a-s-prishchepkoj?ysclid=ma27og9c7a156344069)

> ⚙️ **Метод**: программатор CH341A + прищепка (SOP8 clip)

---

## 📊 Способы прошивки — кратко

| Способ | Метод | Сложность |
|:------:|-------|:------:|
| 1 | Кнопка «Настройка» + питание | ⭐ Лёгкий |
| 2 | CH341A с прищепкой | ⭐⭐ Средний |


---

## ⚠️ Важное примечание

> При использовании **ESPHome** для прошивки через USB-UART адаптер, убедитесь, что устройство переведено в режим загрузки (способ 1).

---

## 📦 Что вам понадобится

- ✅ USB-UART адаптер (например, CH340G / CP2102)
- ✅ Перемычки (dupont)
- ✅ (для способа 2) Программатор CH341A + прищепка

---

<div align="center">
  <sub>
    💡 Разработано для ESPHome | 
    📦 Требуется ESPHome 2026.4+
  </sub>
</div>
