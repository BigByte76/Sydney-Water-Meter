# Sydney-Water-Meter
Measure your water consumption with the pulse LED on your Sydney water meter


Using a ESP32, KY025 board and a tri coloured LED for status indictation.

Facebook link
https://www.facebook.com/groups/HomeAssistant/permalink/3126492500955432


## Hardware

Components required

- [ESP32][esp32-shop]
- [Dupont Jumpers][dupont-jumpers-shop]
- 3D printed case (see the [case](/case) folder)
- KY025: [KY025-shop]
- LED RGB 5mm 4 pin - Cathode: [Banggood][rgbled-bg-shop]


### Wiring Diagram

In the tables below you will find more information, about how to connect the various components.

#### KY025 Board

How the KY025 board is connected to the ESP32

| KY025 Board | ESP32        
|-------------|--------------
| A0          | NOT USING    
| DO          | D12 (GPIO12) 
| VCC         | 3V3          
| GND         | GND          

#### LED

How the status LED is connected to the ESP board of your choice. For each measured pulse, the LED will briefly flash <span style="color:red">*red*</span> and in case of no WiFi connection, the LED will continue to flash <span style="color:blue">*blue*</span>.

| LED    | ESP32      
|--------|------------
| RED    | D2 (GPIO2) 
| GREEN  | D4 (GPIO4)         |
| BLUE   | D5 (GPIO5) 
| GND    | GND       


<!-- Hardware -->
[esp32-shop]: https://au.banggood.com/Geekcreit-ESP32-WiFi+bluetooth-Development-Board-Ultra-Low-Power-Consumption-Dual-Cores-Pins-Unsoldered-p-1214159.html?rmmds=myorder&cur_warehouse=CN
[dupont-jumpers-shop]: https://au.banggood.com/120pcs-20cm-Male-To-Female-Female-To-Female-Male-To-Male-Color-Breadboard-Jumper-Cable-Dupont-Wire-p-974006.html?rmmds=myorder&cur_warehouse=CN
[KY025-shop]: https://au.banggood.com/KY-025-4pin-Magnetic-Dry-Reed-Pipe-Switch-Magnetron-Sensor-Switch-Module-p-1391348.html?rmmds=myorder&cur_warehouse=CN
[rgbled-bg-shop]: https://au.banggood.com/50pcs-LED-RGB-Common-Cathode-4-Pin-F5-5MM-Diode-p-1016398.html?rmmds=myorder&cur_warehouse=CN
