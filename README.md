# ESP8266-LoLin-NodeMCU-V3

ESP8266 NodeMCU V3 as webserver

## Installation

- NodeMCU Flasher Master [Flasher](https://github.com/nodemcu/nodemcu-flasher/archive/master.zip)
- NodeMCU Firmware [Firmware](https://github.com/sleemanj/ESP8266_Simple/raw/master/firmware/ai-thinker-0.9.5.2-115200.bin)
- Latest Arduino IDE [Arduino](https://www.arduino.cc/download_handler.php?f=/arduino-1.6.13-windows.exe)
- NodeMCU V3
- Micro USB Cable
- LED
- Two cables jumper female to female

## Step 1: Installing the Firmware
- Colokan microUsb dengan NodeMCU dab colok kabel ke laptop
- buka NodeMCU software flasher master folder lalu pilih win32 atau win64 folder sesuaikan dengan komputer kalian. sekarang buka folder Release lalu double klik ESP8266Flasher.
- pilih com port
- pilih config tab
- klik gear kecil dan buka firmware yang mana anda telah downloaded
- pilih advenced tab dan pilih the desired Baudrate contoh saya menggunakan 115200
- pilih the Operation tab dan klik pada Flash Button.

## Step 2: Persiapan Arduino IDE

```
setelah install firmware, saatnya memulai programming dengan ESP8266
```
- Install the Arduino IDE
- buka Arduino IDE softwarenya
- klik File tab dan buka preferences
- di additional Boards Manager URLs tambahkan link berikut (http://arduino.esp8266.com/stable/package_esp8266com_index.json) dan klik OK
- klik  tab Tools>Borads>Boards Manager
- di bagian search field ketik esp8266 lalu klik esp8266 by ESP8266 Community option dan klik Install

## Step 3: Coding

```
sebagai contoh project membuat led blinking dengan NodeMCU board via webserver 
```
- pada arduino IDE klik tab tools>Boards>select NODEMCU 1.0 (ESP - 12E Module)
- masih pada tab tools dan pilih port COM sesuai port.
- rubah code variable ssid yaitu nama wifi anda dan variable password.
- pastikan ledPin = 13; // GPIO13
- sekarang klik button Upload untuk mengupload code ke NodeMCU.
- connect kan led's positif kaki pada D7 pin pada board dan negative ke ground dengan dua kabel female.
- ketika sukses terupload code ke mesin, buka serial monitor dari tab tools>arduino IDE
- pada NodeMCU terdapat 2 button RST dan FLASH, klik RST dan perhatikan serial monitornya
- sesudah connecting wifi akan memperlihatkan IP address.
- copy IP address dan paste di web browser(Edge, Chrome, Firefox dll..)
- webpage akan menampilkan dua buah button ON dan OFF.

