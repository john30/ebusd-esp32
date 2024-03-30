
### Version 2024-03-30, reported as `1[431e]`
* fixes:
  * avoid unnecessary wait when sending to eBUS after successful arbitration


### Version 2024-03-17, reported as `1[4311]`
* features:
  * nicer web UI, better responsive layout
  * new improved architecture for eBUS access
  * detect active host on JTAG ebusd connection
  * add last-modified handling to httpd
  * calibrate adc and add isadc command
  * enhanced some commands
* fixes:
  * allow using eth command without args on blank NVS
  * allow 64 chars in WIFI passwords
  * hide credential input fields unless needed (prevents undesired auto fill by some browsers)
  * avoid unnecessary httpd connection close
  * remove useless logging
* other:
  * updated ESP-IDF to current git


### Version 2024-01-06, reported as `1[4106]`
* features:
  * add station rssi to enhanced info
  * add https option with self-signed certificate
* fixes:
  * slow or missing response to enhanced info when there is no eBUS signal
  * potential fix for JTAG connection (aligned with [b8e8042](https://github.com/espressif/esp-idf/commit/b8e8042))
* other:
  * updated ESP-IDF to current git


### Version 2023-12-23, reported as `1[3c17]`
* fixes:
  * fix http server when Ethernet is configured only
* other:
  * updated ESP-IDF to current git


### Version 2023-12-17, reported as `1[3c11]`
* features:
  * add ping + ip REPL commands
  * improve transfer speed for HTTP requests
  * force full WIFI calibration and disable WIFI power save
  * add OTA with 2 swappable partitions
* fixes:
  * memory leak on REPL help command
* other:
  * updated ESP-IDF to current git


### Version 2023-10-15, reported as `1[3a0f]`
* features:
  * add full scan of WIFI to find the strongest AP, fade blue LED while doing so during boot
  * add AP ID to scan and query commands
  * add better startup logging
* fixes:
  * fix BTN press to skip normal boot detection while LEDs fade during boot
  * fix reset upon BTN press when normal boot was skipped
  * fix old I2C driver message
* other:
  * updated ESP-IDF to current git


### Version 2023-09-17, reported as `1[3911]`
* features:
  * add update check to web UI
* fixes:
  * fix optimize handling of host TCP socket
  * fix increase wait time for debouncing BTN press
  * fix increase API request timeouts in web UI
  * fix httpd not started with fix IP and Ethernet only
  * fix too many open sockets in httpd
  * fix potential bytes not sent to host via JTAG serial or UART or to eBUS
* other:
  * updated ESP-IDF to current git


### Version 2023-09-03, reported as `1[3903]`
* features:
  * add option to adjust the bitrate used for eBUS
  * add measurement of bitrate on eBUS and arbitration delay by master
* fixes:
  * fix credentials not being used for API calls by web UI
  * fix invalid value type for number fields in web UI
  * fix use of settings with an empty string
  * fix using a fixed IP
* other:
  * updated web UI packages


### Version 2023-08-15, reported as `1[380f]`
* features:
  * turn off station when configuring Ethernet via IMPROV
* fixes:
  * fix for empty user name forcing HTTP authentication
  * fix not executed reboot on button long press
* other:
  * updated ESP-IDF to current git


### Version 2023-08-06, reported as `1[3806]`
* features:
  * add optional HTTP authentication for sensitive endpoints
  * no longer start AP automatically for 2 minutes (AP mode can still be entered by pressing button during boot)
* fixes:
  * fix potential reboot loop when set to USB
* other:
  * updated ESP-IDF to current git
  * updated web UI packages


### Version 2023-06-18, reported as `1[3612]`
* features:
  * allow setting enhanced/non-enhanced protocol, LED usage and arbitration delay from web
  * smaller enhancements to web UI, better responsive layout
* other:
  * updated ESP-IDF to current git
  * updated web UI packages


### Version 2023-05-01, reported as `1[3501]`
* feat: first version with support for:
  * all eBUS host connection types: WIFI, Ethernet, Raspi, and USB
  * enhanced and non-enhanced protocol
  * flashing and basic setup (IMPROV) via web including Ethernet
  * "easi>" config via web and serial REPL
  * reading 1-wire DS18B20
  * reading BMP180, BMP180, BME280 (REPL only)
  * control of LEDs and LED strip (REPL only)
  * optional SSD1306 for status display (REPL only)


