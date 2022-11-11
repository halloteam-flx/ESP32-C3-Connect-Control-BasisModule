# ESP32C3
! developing embedded system using ESP32-C3 based chip module


_please see the starred projects within this GitHub Account for code-examples_


## technical bottleneck
* pairing between two BLE (bluetooth low energy) notes
* Secure boot and over-the-air (OTA) updates
* Gateway
* APP Develop

## Security
ESP-IDF provides two different secure boot schemes for different revisions of ESP32. Secure boot v1 is for our ESP32C3 chip. 
Secure boot and flash encryption are not reversible. Therefore, only apply them to production devices.
https://docs.espressif.com/projects/esp-idf/en/latest/esp32/security/secure-boot-v1.html
[book Developing IoT Projects with ESP32]
Secure boot is the way we make sure our devices run only our firmware and prevent third parties from tampering with our devices.
The boot process has three stages:
* 1 First-stage bootloader
* 2 Second-stage bootloader
* 3 Application startup


## Updating OTA
One security best practice is that we need to set a mechanism to update firmware of devices in the field. If we find a vulnerability after installation, calling all devices back would be quite costly. Instead, the devices can check an online server to see whether there is new firmware or not and then download and activate any updates. [book Developing IoT Projects with ESP32]

### most frequently used commands ESP-IDF:
```
idf.py set-target esp32c3
idf.py menuconfig
idf.py build
idf.py -p PORT flash
idf.py monitor
```


## IDE substitute for ESP-IDF:
* Arduino-ESP32  
https://espressif-docs.readthedocs-hosted.com/projects/arduino-esp32/en/latest/getting_started.html
* PlatformIO 
https://docs.platformio.org/en/latest/


### ESP-IDF official documents:
https://docs.espressif.com/projects/esp-idf/en/latest/esp32/get-started/index.html

### Espressif DevCon2022 Talk:
https://www.youtube.com/c/EspressifSystems/featured


### recommanded books and tutorials
* https://randomnerdtutorials.com/getting-started-with-esp32/
* https://issuu.com/eimworld/docs/preview_the_official_esp32_book/2?ff






Frequently used Git Commands
```
git add .
git commit -m 'what have you done'
git push

git checkout 
git pull
```
https://www.freecodecamp.org/news/10-important-git-commands-that-every-developer-should-know/
(because this is a private repo you need to download in a specific way)
```
git clone https://halloteam-flx@github.com/halloteam-flx/ESP32C3
```
(personal access token) 
```
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
```
