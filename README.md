# An Embedded Weather Quest

### Preparation

**Required Components:**
- TM4C123 LaunchPad
- CC3100 Booster Pack
- An Internet Access Point
- ST7735R 128x160 Color LCD

### Project Description

This system will process user requests from a laptop serial terminal, interact with openweathermap.org for weather data on U.S. cities, and display the obtained weather information on both a laptop serial terminal and a color LCD.

#### User Interface Requirements

The serial terminal interface should prompt users with the following options:

```
Welcome to my Embedded Weather Quester!
Please choose your query criteria:
1. City Name
2. City ID
3. Geographic Coordinates
4. Zip Code
```

**Information to Display:**
- Temperature of the city
- Humidity of the city
- Weather conditions of the city

**Display Specifications:**

*Serial Terminal Display:*
- Temperature minimum: 50°F
- Temperature maximum: 80°F
- Humidity: 69
- Weather: sunrise

*Color LCD Display:*
- Text on the left displaying temperature range, humidity, and weather.
- Animation on the right side for three weather conditions: Sunrise, Cloudy, Rainy.

### Getting Ready for the Project

[cc3100_quick_start_guide](cc3100_quick_start_guide.pdf)  
[City List (JSON) for OpenWeatherMap](city.list.json.gz)  
[Starter Project](WeatherQuesterStarter.zip)

How to find an access point: Turn on the hot spot, then you will have an access point from your phone. Both iPhone and Samsung phones by default use WPA encryption. You can also change the encryption. Make sure there is no space in your access point name.

We can use city ID to query the weather. See a list of city IDs in the attached file: city.list.json.gz. You need to unzip it and then use notepad or notepad plus to open it.

Syntax for using city ID to access weather information for the city:

```C
#define REQUEST "GET /data/2.5/weather?id=5367929&APPID=83dc682a0126fd6a9bb93b6eb3e6a7eb&units=metric HTTP/1.1\r\nUser-Agent: Keil\r\nHost:api.openweathermap.org\r\nAccept: */*\r\n\r\n"
```

The above example is for accessing Long Beach, CA, US

You can find the Get command format on the following link at openweathermap website:

https://openweathermap.org/currentLinks to an external site.

The following link gives you a list of condition ids:

https://openweathermap.org/weather-conditionsLinks to an external site.

You can find raining cities at the following website: https://www.rainviewer.com/Links to an external site.

## Preparation:
1. `TM4C123` LaunchPad
2. `CC3100` Booster Pack
3. Setup access point
4. `ST7735R` 128x160 Color LCD.
5. Setup `OpenWeatherMap API key` `(APPID)`. 

## Steps to Setup Access Point:
1. Setup mobile hotspot on your device. (Laptop, phone, etc.)
2. Connect to the hotspot with the `CC3100` Booster Pack by editing the main file. 
```C
// To Do: replace the following three lines with your access point information
#define SSID_NAME  "WIFI_NAME" /* Access point name to connect to */
#define SEC_TYPE   SL_SEC_TYPE_WPA
#define PASSKEY    "password"  /* Password in case of secure AP */ 
```

## Steps to Get Access to OpenWeatherMap:

In order to have your smart object interact with **openweathermap.org**, you need to register then get an API key. The following steps will guide you through the process:
1. Go to https://openweathermap.org/appid
2. Register on the sign up page for a free account.
3. Sign in and get your API key (APPID) from the the server. (Located when clicking on your username in the top right corner)
4. Copy the API key to main file within the `REQUEST` macro.
    - #define REQUEST "GET /data/2.5/weather?id=5367929&APPID=`PASTHERE`&units=metric HTTP/1.1\r\nUser-Agent: Keil\r\nHost:api.openweathermap.org\r\nAccept: */*\r\n\r\n"

