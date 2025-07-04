### Version 2025-06-15, reported as `1[560f]`
* features:
  * add Home Assistant integration via MQTT discovery including update entity
  * add follow log option to UI
  * add better responsive UI
  * add faster transfer via MQTT with QoS 0
* fixes:
  * fix extended MQTT URI storage
* other:
  * updated ESP-IDF to [v5.3.3 release on commit d1159f6](https://github.com/espressif/esp-idf/commit/d1159f634d138f446625a585fc0c77ecee0bcfcb)


### Version 2025-05-17, reported as `1[5511]`
* features:
  * add option to skip Ethernet module check
  * add extended MQTT URI length
  * add watchdog
* fixes:
  * fix weird REPL in web serial
* other:
  * updated ESP-IDF to [v5.3.3 release on commit 995b09e](https://github.com/espressif/esp-idf/commit/995b09e792b01369597d999dc24c52f8ff8b4681)


### Version 2025-04-15, reported as `1[540f]`
* features:
  * add option to erase other partition to UI and "ota" command
* other:
  * updated mDNS component
  * updated ESP-IDF to [v5.3.3 release on commit 60d077e](https://github.com/espressif/esp-idf/commit/60d077eaddd070ba507dfdb160131b184d2804c6)


### Version 2025-02-16, reported as `1[5210]`
* features:
  * turn off red LED when WPS succeeded
  * drop irrelevant logging during boot
  * add ADC inputs to UI
  * add option to send pin status and sensors to MQTT
  * nicer UI
* fixes:
  * fix IMPROV transfer including newline chars (e.g. for scan result)
  * fix reset in "strip" command
* other:
  * updated mDNS component
  * updated ESP-IDF to [v5.3.2 release on commit a916a25](https://github.com/espressif/esp-idf/commit/a916a250ea6ffc28ce036e1ba2558e6c5b2043c9)


### Version 2025-01-20, reported as `1[5114]`
* features:
  * start WPS after button press only when device is unconfigured and add WPS status to query command
* other:
  * updated mDNS component
  * updated ESP-IDF to [v5.3.2 release on commit adf5319](https://github.com/espressif/esp-idf/commit/adf5319639b7e66e4f80868b14fee1acb73672c7)


### Version 2024-12-21, reported as `1[4c15]`
* features:
  * nicer UI
* fixes:
  * fix wifi scan and join while wps enabled
  * fix previous build (20241215) with mismatched bundled UI
* other:
  * updated mDNS component
  * updated ESP-IDF to [v5.3.2 release on commit 083aad9](https://github.com/espressif/esp-idf/commit/083aad99cfc1a7981009ac7f18e29824c47ffba2)


### Version 2024-10-27, reported as `1[4a1b]`
* features:
  * add retrieval of credentials from WPS with push button mode (PBC) when device is blank
  * add mDNS device string to the UI
  * add Wi-Fi 6 only protocol selection on C6
* fixes:
  * arbitrary reboots issued by RGB LED driver
  * mDNS service list in case of late station connection
* other:
  * updated ESP-IDF to [v5.3.1 release on commit a0f798c](https://github.com/espressif/esp-idf/commit/a0f798cfc4bbd624aab52b2c194d219e242d80c1)


### Version 2024-10-08, reported as `1[4a08]`
* features:
  * add estimate bus voltage report to enhanced protocol
  * add average of several samples for adc command
* other:
  * updated ESP-IDF to [v5.3.1 release on commit 707d097](https://github.com/espressif/esp-idf/commit/707d097b01756687cca18be855a2675d150247ae) (including the massively changed USB serial driver)



### Version 2024-08-25, reported as `1[4819]`
* features:
  * better responsive web UI
  * add mDNS for auto discovery
* fixes:
  * HW ID determination for C6
* other:
  * updated ESP-IDF to [commit 0bbd728](https://github.com/espressif/esp-idf/commit/0bbd72819602b4b8cf786a8833d0ee9c922268bf) (without the massively changed USB serial driver though)


### Version 2024-08-09, reported as `1[4809]`
* features:
  * first version also released for ESP32-C6 supporting the [C6 Edition](https://adapter.ebusd.eu/v5-c6/index.en.html)
* other:
  * updated ESP-IDF to released [v5.3 version](https://github.com/espressif/esp-idf/tree/release/v5.3) on [commit dc7fb34](https://github.com/espressif/esp-idf/commit/dc7fb34fca8d4a7b7232772458931072f44c3264) (without the massively changed USB serial driver though)


### Version 2024-06-15, reported as `1[460f]`
* features:
  * add logging of last data exchanged to/from eBUS/host on error log and in verbose mode
* fixes:
  * enable another WiFi optimization setting of ESP-IDF to improve TCP transfer
  * remove one case reported as host protocol error, that is actually in responsibility of ebusd and not the adapter
* other:
  * updated ESP-IDF to current git ([release/v5.3 branch](https://github.com/espressif/esp-idf/tree/release/v5.3)) on [commit ae87691](https://github.com/espressif/esp-idf/commit/ae876915ec7aa0f96edc826e413baa45ac3c2a64)


### Version 2024-05-26, reported as `1[451a]`
* features:
  * first version also released for [Wemos C3 mini](wemos.en) for use on older adapters
  * improved workaround for skipping too lengthy HTTP request headers (for weird cloudflare tunneling)
  * show initial network connection as green fade off
  * smaller web UI improvements
  * use dedicated reset pin for USR-ES1/W5500 Ethernet
* fixes:
  * missed reboot from web UI when skipping startup procedure
* other:
  * updated ESP-IDF to current git ([release/v5.3 branch](https://github.com/espressif/esp-idf/tree/release/v5.3))


### Version 2024-05-18, reported as `1[4512]`
* features:
  * nicer web UI, better responsive layout for the pins section
  * skip too lengthy HTTP request headers (workaround for weird cloudflare tunneling)
* fixes:
  * correct topic extraction on received MQTT messages


### Version 2024-05-05, reported as `1[4505]`
* features:
  * improve timers and async handling of timed tasks (MQTT, LEDs)
  * force full Wi-Fi calibration
  * add wifi power+protocol+channel selection
  * more verbose "query" and "ip" command output
  * remove annoying vfs warning
  * add workaround for DNS via DHCP
  * increase tolerated HTTP header length
  * disable queueing TCP out-of-order packets
  * nicer web UI, better responsive layout
* other:
  * updated ESP-IDF to current git ([release/v5.3 branch](https://github.com/espressif/esp-idf/tree/release/v5.3))


### Version 2024-04-20, reported as `1[4414]`
* features:
  * add ps command
* other:
  * switched ESP-IDF to [release/v5.3 branch](https://github.com/espressif/esp-idf/tree/release/v5.3) and updated to latest


### Version 2024-04-15, reported as `1[440f]`
* features:
  * MQTT support with status info like version, uptime, eBUS signal, temperature, AP RSSI
  * configurable HTTPS certificate
* other:
  * updated ESP-IDF to current git


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
