# Changelog

All notable changes to this project will be documented in this file.

## [2.0.0] - 2026-03-25

### FEAT

* Add new LED effects
* Add automatic light turn-off delay (adelay_off_init_pir_day / delay_off_init_pir_night) based on sunrise/sunset

### FIX

* Fix light state handling (current_option()) in script_lights.yaml
* Disable reboot on API timeout
* Fix wifi_signal_db attribute reporting

### IMP

* Update LED brightness in real time when changed by the user
* Update LED effect in real time when changed by the user
* Refactor and update LED effects implementation
* Increase CPU frequency to 240 MHz for improved performance
* Reduce flash write interval to 10 minutes for better stability
* Adjust reboot timeout for WiFi/AP
* Move binary_sensor to separate file
* Bump web_server version to 3
* Add additional debug sensors
