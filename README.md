# Sydney-Water-Meter
Measure your water consumption with the magnetic flow sensor on your Sydney water meter.

This works by calculating how many pulses your water meter does for every 1L of water. The code is based off one pulse for every 0.5L of water.


## Common Parts

The below parts are recommended for both the Zigbee and ESP version
- [Waterproof Enclosure] [case-shop]
- [Cable Gland] [gland-shop]
- Required length of 2 core wire
- [Reed Switch] [reed-switch]

## Zigbee Version Setup

Components required

- [Aqara Door Window Sensor] [Zigbee-sensor]

Remove the reed switch from the sesnor board and solder the required lenght of wire in its place and the other end of wire to a reed switch making sure the exposed leads are covered with heat shrink.

See water-meter-zigbee-YAML file for home assistant code.

## ESP Version Setup

## I have not tried this yet as I use the zigbee version ##

Using a ESP32, KY025 board and a tri coloured LED for status indictation.

### Hardware

Components required

- [ESP32][esp32-shop]
- [Dupont Jumpers][dupont-jumpers-shop]
- KY025: [KY025-shop]
- LED RGB 5mm 4 pin - Cathode: [Banggood][rgbled-bg-shop]


### Wiring Diagram

In the tables below you will find more information, about how to connect the various components.

##### KY025 Board

Remove the reed switch from the KY025 board and solder the required lenght of wire in its place and the other end of wire to a reed switch making sure the exposed leads are covered with heat shrink.

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

See water-meter.yaml for ESPHome code

<!-- Hardware -->
[esp32-shop]: https://au.banggood.com/Geekcreit-ESP32-WiFi+bluetooth-Development-Board-Ultra-Low-Power-Consumption-Dual-Cores-Pins-Unsoldered-p-1214159.html?rmmds=myorder&cur_warehouse=CN
[dupont-jumpers-shop]: https://au.banggood.com/120pcs-20cm-Male-To-Female-Female-To-Female-Male-To-Male-Color-Breadboard-Jumper-Cable-Dupont-Wire-p-974006.html?rmmds=myorder&cur_warehouse=CN
[KY025-shop]: https://au.banggood.com/KY-025-4pin-Magnetic-Dry-Reed-Pipe-Switch-Magnetron-Sensor-Switch-Module-p-1391348.html?rmmds=myorder&cur_warehouse=CN
[rgbled-bg-shop]: https://au.banggood.com/50pcs-LED-RGB-Common-Cathode-4-Pin-F5-5MM-Diode-p-1016398.html?rmmds=myorder&cur_warehouse=CN
[Zigbee-sensor]: https://www.aliexpress.com/item/32991903307.html?spm=a2g0o.order_list.0.0.42611802kYyjMQ
[case-shop]: https://www.aliexpress.com/item/4000242432947.html?spm=a2g0o.order_list.0.0.42611802kYyjMQ
[gland-shop]: https://www.aliexpress.com/item/4000242432947.html?spm=a2g0o.order_list.0.0.42611802kYyjMQ
[reed-switch]: https://www.aliexpress.com/item/4000773848015.html?spm=a2g0o.productlist.0.0.341b759cy7X1y2&algo_pvid=9a549358-1722-4ee8-a29d-80e92bca3703&algo_exp_id=9a549358-1722-4ee8-a29d-80e92bca3703-3&pdp_ext_f=%7B%22sku_id%22%3A%2210000007741367206%22%7D&pdp_npi=2%40dis%21AUD%211.26%211.14%21%21%211.59%21%21%4021031a5516684838702068314e3aff%2110000007741367206%21sea&curPageLogUid=UU7Mj9E39Y3I
