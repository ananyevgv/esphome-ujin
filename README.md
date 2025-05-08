[![License][license-shield]][license]
[![ESPHome release][esphome-release-shield]][esphome-release]

[license-shield]: https://img.shields.io/static/v1?label=License&message=MIT&color=orange&logo=license
[license]: https://opensource.org/licenses/MIT
[esphome-release-shield]: https://img.shields.io/static/v1?label=ESPHome&message=2025.3&color=green&logo=esphome
[esphome-release]: https://GitHub.com/esphome/esphome/releases/


# Интегрированные устройства UJIN в ESPHome


# [Lume Luxe L.te M1](https://github.com/ananyevgv/esphome-ujin/blob/main/lume%20L.te%20M1.yaml)

<img src="https://github.com/NagibinA/esphome-ujin-1/blob/5f76cadf9561d7a832881ac16208bb044533d744/Lume%20Luxe_L.te%20M1/images/Luxe_Lte%20M1_1.jpg" height="300" alt="Lume L.te lite">


В прошивке выключателя реализовано:
1. Диммирование двух каналов.

      При включенном диммировании:

      • Однократное (короткое) нажатие включает или выключает лампу с установленной (сохраненной) яркостью.

      • Удерживая сенсорную панель (длинное нажатие), плавно увеличивает или уменьшает яркость лампы. Это прекращается, когда лампа полностью включается или полностью выключается.

      • Отпустив, а затем снова нажав удерживая сенсорную панель, измениться направление, то есть если свет становился тусклее, то, отпустив и снова нажав, он будет ярче.

2. Подключение внешних выключателей в режиме "выключатель"
3. Подсветка сенсорных кнопок адресными светодиодами с выбором цвета и яркости состояния (нажата, включено, выключено)
4. Реализован режим "Ночник" тремя вертикальными, адресными светодиодами, с выбором яркости и цвета
5. В режиме подключения к Wi-Fi, вертикальные светодиоды мигают до подключения к сети
6. Реализован датчик шума с выбором действия по сработке
7. Реализован датчик движения с выбором действия по сработке
8. Подключен датчик освещенности
9. Подключен датчик температуры и влажности
10. Реализован приемник IR  с выбором бренда и отображением принятого кода
11. Подключен передатчик IR
12. Реализована работа ZigBee координатора ZHA

    


# todo: 
      
      1. Отключение диммирования на ходу
      2. Ограничение включения света по датчику освещенности
      3. BLE

# [Lume wifi/BLE/IR/CO2]

<img src="https://github.com/ananyevgv/esphome-ujin/blob/main/image%2Flumi%20co2.jpg" height="300" alt="Lume CO2 lite">

и ему подобными с управлением диммером по цифровому интерфейсу.


# todo: 

      1. Управление диммером
      2. BLE (мало памяти необходимо замена flash)
      3. Отключение диммирования на ходу
      4. Ограничение включения света по датчику освещенности.


# [Connect din](https://github.com/ananyevgv/esphome-ujin/blob/main/rele-ujin.yaml)

<img src="https://github.com/ananyevgv/esphome-ujin/blob/main/image%2Frelay.jpg" height="300" alt="Lume relay">

 
# [Aqua Sense](https://github.com/ananyevgv/esphome-ujin/blob/main/leak-sensor.yaml)

<img src="https://github.com/ananyevgv/esphome-ujin/blob/main/image%2Faqua.jpg" height="300" alt="Lume leak sensor lite">
