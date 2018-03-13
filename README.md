# espaper-weatherstation-pio

This is a repository you can use with platformio and the espaper weatherstation by ThingPulse as sold here: https://thingpulse.com/product/2-9-espaper-plus-kit/ (no affiliate or whatever).

![thedevice](https://github.com/Thijxx/espaper-weatherstation-pio/blob/master/img/ESPaperBoxBezelFrontReflection.jpg)

**Configuration**

These are the settings you need to change in `settings.h` before you upload the code to the device.
```
String WIFI_SSID = "the_neighbours";
String WIFI_PASS = "supersecret";
String DISPLAYED_CITY_NAME = "Leiden";
String WUNDERGRROUND_API_KEY = "0123456789";
String WUNDERGRROUND_LANGUAGE = "en";
String WUNDERGROUND_COUNTRY = "NL";
String WUNDERGROUND_CITY = "Leiden";
```

**Dependancies**

Dependancies should be resolved automatically by platformio. They will be installed when you hit Build in the interface because they are in the **platformio.ini** shown below.

```
[env:esp12e]
platform = espressif8266
board = esp12e
framework = arduino
lib_deps =
  JsonStreamingParser,
  Mini Grafx,
  WeatherStation,
  simpleDSTadjust
```

**Uploading**

Before you put the device in programming mode make sure it has power via USB or a full battery
- Connect FTDI and powersource (turn on or connect USB power)
- Hold middle button
- Press right button briefly
- Release both
- Hit Upload in Platfomrio

![back](https://github.com/Thijxx/espaper-weatherstation-pio/blob/master/img/PCBBackReflectionWithLegend.jpg)
![front](https://github.com/Thijxx/espaper-weatherstation-pio/blob/master/img/PCBFrontReflectionWithLegend.jpg)
