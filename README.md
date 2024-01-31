# An Embedded Weather Quest

### Preparation

**Required Components:**
- TM4C123 LaunchPad
- CC3100 Booster Pack
- An Internet Access Point
- ST7735R 128x160 Color LCD

### Project Description

In this project, titled "An Embedded Weather Quest," students will leverage the knowledge acquired throughout the semester and previous courses to build an IoT application. The application aims to demonstrate proficiency in several key embedded systems topics, including GPIO, Interrupts, Hardware Timers, UART, Color LCDs, SSI, and WiFi.

Students will construct an embedded system capable of WiFi communication. This system will process user requests from a laptop serial terminal, interact with openweathermap.org for weather data on U.S. cities, and display the obtained weather information on both a laptop serial terminal and a color LCD.

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

1. **Hardware Setup:** Stack the TM4C123 LaunchPad and CC3100 Booster Pack, and connect the ST7735R LCD.
2. **Software Setup:**
-Register and note your APPID from openweathermap.org.
-Replace the APPID placeholder in your project with the actual ID.
-Configure your device to connect to an internet access point.
-Test the setup using a serial terminal at 115200 baud rate.


