[![License][license-shield]][license]
[![ESPHome release][esphome-release-shield]][esphome-release]

[license-shield]: https://img.shields.io/static/v1?label=License&message=MIT&color=orange&logo=license
[license]: https://opensource.org/licenses/MIT
[esphome-release-shield]: https://img.shields.io/static/v1?label=ESPHome&message=2025.3&color=green&logo=esphome
[esphome-release]: https://GitHub.com/esphome/esphome/releases/


# Интегрированные устройства UJIN в ESPHome


| [Lume Luxe L.te M1](https://github.com/Ananyevgv/esphome-ujin/blob/7df921a225203874b50efc2a2f6a108fb8cb2985/Lume%20Luxe_L.te%20M1/lume%20luxe%20L.te%20M1.yaml)  |  [Lume Wi-Fi Z1](https://github.com/ananyevgv/esphome-ujin/blob/main/Lume%20Wi-Fi_Z1/lume%20WIFI%20Z1.yaml) | [Lume wifi/BLE/IR/CO2](https://github.com/ananyevgv/esphome-ujin/blob/main/Lume%20Wi-Fi_BLE_IR_CO2) | Lume Luxe L.te M2 | 
|--------------------|---------------|----------------------|-------------------|
| ![Lume Luxe L.te M1](https://github.com/Ananyevgv/esphome-ujin/blob/5f76cadf9561d7a832881ac16208bb044533d744/Lume%20Luxe_L.te%20M1/images/Luxe_Lte%20M1_1.jpg) | ![Lume Wi-Fi Z1](https://github.com/ananyevgv/esphome-ujin/blob/main/Lume%20Wi-Fi_Z1/Lume%20WIFI%20Z1.jpg) | ![Lume wifi/BLE/IR/CO2](https://github.com/ananyevgv/esphome-ujin/blob/main/Lume%20Wi-Fi_BLE_IR_CO2/images/Lume%20wifi_BLE_IR_CO2_1.jpg) | ![Lume Luxe L.te M2](https://github.com/ananyevgv/esphome-ujin/blob/main/Lume%20Luxe_L.te%20M2/Lume%20Luxe_L.te%20M2.jpg) |


| [Connect din](https://github.com/Ananyevgv/esphome-ujin/blob/f9e8dd99a58445ae1349fafaf5a36c6e7d8ec50f/Connect-din%20Wi-Fi/rele-ujin.yaml)        | [Aqua Sense](https://github.com/Ananyevgv/esphome-ujin/blob/02668abdb31d5efbcec2e42ae0b62cf414c559d0/Aqua-Sense%20BLE/leak-sensor.yaml)    | [Heat Wi-Fi](https://github.com/ananyevgv/esphome-ujin/blob/main/Heat%20Wi-Fi%2Fheat_wifi.yaml)           |   [Aqua Wi-Fi BLE 220В СУ-02 R2](https://github.com/ananyevgv/esphome-ujin/blob/ab583b7662ee3f60981c07a3cfd8f1724de03bbe/Aqua%20Wi-Fi_BLE_220%D0%92_%D0%A1%D0%A3-02_R2/Aqua%20Wi-Fi_pinout.txt)       | 
|--------------------|---------------|----------------------|-------------------|
| ![Connect din](https://github.com/ananyevgv/esphome-ujin/blob/main/Connect-din%20Wi-Fi/images/connect-din_wi-fi.jpg) | ![Aqua Sense](https://github.com/ananyevgv/esphome-ujin/blob/c8646eea51e237678c43588dae4a290cfe0a1586/Aqua-Sense%20BLE/images/Aqua-Sense%20BLE.jpg) | ![Heat Wi-Fi](https://github.com/Ananyevgv/esphome-ujin/blob/382708609ab669d9a017be2ed7dc692cb6605322/Heat%20Wi-Fi/images/heat_1.jpg) | ![Aqua Wi-Fi](https://github.com/ananyevgv/esphome-ujin/blob/c8646eea51e237678c43588dae4a290cfe0a1586/Aqua%20Wi-Fi_BLE_220%D0%92_%D0%A1%D0%A3-02_R2/images/Aqua%20Wi-Fi_1.jpg) |





# [Lume Luxe L.te M1](https://github.com/Ananyevgv/esphome-ujin/blob/7df921a225203874b50efc2a2f6a108fb8cb2985/Lume%20Luxe_L.te%20M1/lume%20luxe%20L.te%20M1.yaml)

В этом выключателе, ипользуется прямое управление диммером (с отслеживанием нуля).

В прошивке выключателя реализовано:
1. Диммирование двух каналов.

      При включенном диммировании:

      • Однократное (короткое) нажатие включает или выключает лампу с установленной (сохраненной) яркостью.

      • Удерживая сенсорную панель (длинное нажатие), плавно увеличивает или уменьшает яркость лампы. Это прекращается, когда лампа полностью включается или полностью выключается.

      • Отпустив, а затем снова нажав удерживая сенсорную панель, измениться направление, то есть если свет становился тусклее, то, отпустив и снова нажав, он будет ярче.

2. Подключение внешних сущностей light из HA с поддержкой димирования и без.
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

    




# to do: 
      
      1. BLE




Версия платы 2.3 с датчиками css811, sht30, bh1750

Версия платы 2.4 с датчиками bme680, bh1750

# [Lume Luxe L.te M2]

В этих выключателях, управление диммером происходит по UART 115200 8n1 (+LOG).

# to do: 

      1. Управление диммером
      2. BLE (мало памяти необходимо замена flash)



