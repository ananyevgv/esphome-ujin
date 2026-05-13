[![License][license-shield]][license]
[![ESPHome release][esphome-release-shield]][esphome-release]

[license-shield]: https://img.shields.io/static/v1?label=License&message=MIT&color=orange&logo=license
[license]: https://opensource.org/licenses/MIT
[esphome-release-shield]: https://img.shields.io/static/v1?label=ESPHome&message=2026.4&color=green&logo=esphome
[esphome-release]: https://GitHub.com/esphome/esphome/releases/

<div align="center">
  <h1>🔧 Приводы UJIN</h1>
  <p><strong>Шаровые краны с электроприводом для систем водоснабжения</strong></p>
  <br/>
</div>


---

## 📌 Модификации приводов

Приводы UJIN выпускаются в **двух вариантах исполнения**:

| Модификация | Напряжение | Особенности |
|-------------|------------|-------------|
| **220V** | 220В переменного тока | ⚠️ Имеет встроенный блок питания (мотор на **5В**) |
| **12V** | 12В постоянного тока | Прямое питание |

<div align="center">
  <table>
    <tr>
      <td align="center"><img src="./images/board_220v.jpg" width="250"><br/><sub>Плата 220V</sub></td>
      <td align="center"><img src="./images/drive_12V.jpg" width="250"><br/><sub>Привод 12V</sub></td>
    </tr>
  </table>
</div>

> 🫣 **Комментарий к модификации 220В**  
> Внутри установлен блок питания, а мотор рассчитан на **5В** ([посмотреть фото](./images/board-220_0.jpg))

---

## 🔧 Доработка: контроль состояния

Вы можете добавить **микропереключатель (end-stop)** для контроля положения привода (открыт/закрыт).

| Фото |
|------|
| [![Микропереключатель 1](./images/drive_1.jpg)](./images/drive_1.jpg) |
| [![Микропереключатель 2](./images/drive_3.jpg)](./images/drive_3.jpg) |

---

## 📷 Внешний вид

<div align="center">
  <img src="/drive/images/drive.jpg" width="400">
  <br/>
  <sub>Привод UJIN в сборе</sub>
</div>

---

## 🌊 Проект «Зимняя вода для улицы с автосливом»

Готовое решение для защиты системы водоснабжения от замерзания в зимний период.

| Проект | Описание |
|--------|----------|
| [❄️ Winter water](/drive/winter_water) | Автоматический слив воды + управление приводом |

---

## 📊 Спецификация

| Параметр | 220V | 12V |
|----------|:----:|:---:|
| Питание мотора | 5В (через БП) | 12В |
| Тип тока | Переменный | Постоянный |
| Встроенный БП | ✅ | ❌ |
| Управление | ESPHome / реле | ESPHome / реле |
| Контроль положения | опционально (микропереключатель) | опционально |

---

## ⚠️ Важные замечания

| № | Примечание |
|:--:|------------|
| 1 | Версия **220V** имеет мотор на **5В** — учитывайте при замене драйвера |
| 2 | Для контроля состояния привода рекомендуется добавить **микропереключатель** |
| 3 | Проект «Зимняя вода» включает готовую автоматику для улицы |

---

<div align="center">
  <sub>
    💡 Разработано для ESPHome | 
    📦 Требуется ESPHome 2026.4+
  </sub>
</div>
