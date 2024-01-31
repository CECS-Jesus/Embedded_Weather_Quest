
# CECS 447 Embedded Systems III Final Project

## An Embedded Weather Quest

**Total Points:** 15

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

**Starter Project:** WeatherQuest

1. **Hardware Setup:** Stack the two boards and connect the Nokia LCD.
2. **Project Setup:** Download and unzip `WeatherQuest.zip`, open the project in `CC3100GetWeather_4C123`, and recompile.
3. **Testing:** Modify and test both `main.c` and `mainNokia5110.c` programs as per the instructions below:
   - Register for an account at [openweathermap.org/appid#use](http://openweathermap.org/appid#use) and note the APPID.
   - Replace `APPID` in the project with your unique ID.
   - Set up and connect to an access point using a phone or laptop.
   - Recompile and test using a serial terminal at 115200 baud rate.
4. **LCD Replacement:** Substitute the Nokia5110 with the ST7735 color LCD.
5. **Project Development:** Begin with the working example project and integrate the required features.

### Grading Policy

**Demonstration:** 10 Points
- Display hardcoded city query on laptop and LCD, with one animation: 60%
- Add two additional animations: 10%
- Implement user choice for query criteria: 30%

**Report + Source Code:** 5 Points

### Deliverables

1. **Demonstration:** Present the embedded system to the instructor.
2. **Final Project Report:** Submit in Word or PDF format, including sections on Operation (with video link), Hardware Design (with schematic and system picture), and any other required information.
3. **Source Code:** Submit `mainST7735.c`, `ST7735.c/h`, and any additional component code in a zip file.
