# esp-idf-switch-access-points
Switching access points for esp-idf.

Station mode of esp-idf cannot connect to multiple access points at the same time.   
However, it is possible to switch access points sequentially:   
AP1->AP2->AP1->AP2   

This is example code that switches access points sequentially.   

# Software requiment   
ESP-IDF V5.0 or later.   
ESP-IDF V4.4 release branch reached EOL in July 2024.   

# Install
```
git clone https://github.com/nopnop2002/esp-idf-switch-access-points
cd esp-idf-switch-access-points
idf.py menuconfig
idf.py flash monitor
```

# Firmware configuration
You have to set this config value using menuconfig.   

- CONFIG_ESP_WIFI_SSID1   
SSID of your wifi AP1.
- CONFIG_ESP_WIFI_PASSWORD1   
PASSWORD of your wifi AP1.
- CONFIG_ESP_WIFI_SSID2   
SSID of your wifi AP2.
- CONFIG_ESP_WIFI_PASSWORD2   
PASSWORD of your wifi AP2.
- CONFIG_ESP_MAXIMUM_RETRY   
Maximum number of retries when connecting to wifi.

![config-1](https://user-images.githubusercontent.com/6020549/101636668-01bee280-3a6f-11eb-961b-9919e1e0eef0.jpg)

![config-2](https://user-images.githubusercontent.com/6020549/101636847-3d59ac80-3a6f-11eb-9324-07919d60ce46.jpg)
