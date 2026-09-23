---
title: "RootMaker Arduino API"
description: ""
tags: "Arduino,API,lib"
published: true
isPublished: true
---
<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Dev/img/rootmaker_main_image.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

RootMaker is the first development board in the Ryzobee series. Based on the ESP32-S3, it integrates an LCD, touch input, an RGB LED, an accelerometer, a button, and battery management for interactive 3D-printed creations and creative electronics projects.

<div style="border-left: 6px solid #ff6a00;background: #fff7ed;padding: 10px 16px; border-radius: 0px;">
  <h3 class="toc-header" style="margin-top: 0px; color:#FFA00;"><a href="https://github.com/Ryzobee" class="toc-anchor"></a>📘<a style="color: #FF6A00; text-decoration: none;"> RootMaker Product Specifications</a></h3>
  <p style="margin-bottom: 10px;">
  If you are new to RootMaker, visit the RootMaker product wiki page.
  </p>
<div style="text-align: center;"><a href="/en/root/rootmaker/rootmaker" target="_blank" style="display: inline-block; padding: 4px 25px; background: #FF6A00; color: rgb(255, 255, 255); border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none; border-radius: 50px; font-weight: bold; text-decoration: none; transition: transform 0.2s; margin: 5px; box-shadow: none;">
    Go to the RootMaker Product Wiki →
    </a></div></div>

## Hardware Specifications

| Item | Description |
|:---:|:---|
| MCU | ESP32-S3 |
| Flash | 16MB (QIO 80MHz) |
| PSRAM | 2MB QSPI PSRAM |
| LCD | SPI / ST7789, 240×240 |
| Touch | CST816T capacitive touch |
| LED | WS2812B RGB LED |
| Sensor | LIS2DWTR 3-axis accelerometer |
| Button | Onboard user button (GPIO0) |
| Battery Management | TP4054 charging + PY32 battery monitoring |
| Expansion Ports | 4 RS-Port interfaces (I2C) |

## Arduino IDE Configuration

| Item | Setting |
|:---:|:---:|
| Board | ESP32S3 Dev Module |
| Flash Mode | QIO 80MHz |
| Flash Size | 16MB |
| PSRAM | 2MB |

## Quick Start

```cpp
#include "Ryzobee.h"

Ryzobee board(RYZOBEE_ROOTMAKER);

void setup(void)
{
    Serial.begin(115200);
    board.rootmaker.begin();
}

void loop(void)
{
    // Your code here
}
```

### begin() Parameters

The `begin()` method lets you enable modules as needed:

```cpp
void begin(bool LCDEnable      = false, 
           bool LEDEnable      = true, 
           bool SensorEnable   = true, 
           bool ButtonEnable   = true,
           bool BatteryEnable  = true);
```

| Parameter | Default | Description |
|:---:|:---:|:---|
| LCDEnable | false | Enable the LCD and touch input |
| LEDEnable | true | Enable the WS2812B RGB LED |
| SensorEnable | true | Enable the LIS2DWTR accelerometer |
| ButtonEnable | true | Enable the onboard button |
| BatteryEnable | true | Enable battery management |

> **Note:** The LCD is disabled by default. Enable it explicitly when you need the display.

## Example Programs

The Ryzobee library includes examples covering all onboard peripherals of the RootMaker development board.

### Open Examples in the Arduino IDE

1. Open the Arduino IDE.
2. Select **File > Examples**.
3. Scroll to the **Ryzobee** category.
4. Select the example you want to open.

### Available Examples

| Example | Function |
|:---:|:---|
| battery | Monitor battery level; indicate level through LED color and display voltage and charging status on screen |
| btn | Detect button events (short press / long press / double click / hold) |
| gif | Play GIF animations and switch animations with the button |
| i2c_scan | Scan for I2C devices on the 4 RS-Port expansion interfaces |
| led | RGB LED rainbow cycle effect |
| lis2dwtr | Read XYZ data from the LIS2DWTR accelerometer |
| screen | Touchscreen interaction: a simple tap-to-move block game |

### Steps

1. Open an example through **File > Examples > Ryzobee**.
2. Select `ESP32S3 Dev Module` under **Tools > Board**.
4. Connect the RootMaker board with a USB cable.
5. Select the corresponding serial port under **Tools > Port**.
6. Click Upload to flash the program.

> **Tip:** Start with the `led` or `btn` example to verify your development environment before trying more complex examples.

## Peripheral Guide

### LCD Display

RootMaker includes a 240×240 ST7789 SPI LCD and a CST816T capacitive touch controller. The LCD module wraps the LovyanGFX graphics library.

#### Initialization

```cpp
board.rootmaker.begin(true, false, false, false, false); // Enable LCD only

board.rootmaker.lcd->setBrightness(255);  // Set backlight brightness (0-255)
board.rootmaker.lcd->fillScreen(TFT_BLACK);  // Clear the screen
```

#### Display Text

```cpp
board.rootmaker.lcd->setTextSize(2);
board.rootmaker.lcd->setTextColor(TFT_WHITE, TFT_BLACK);
board.rootmaker.lcd->drawString("Hello Ryzobee!", 60, 120);
```

#### Draw Graphics

```cpp
board.rootmaker.lcd->fillRect(x, y, width, height, TFT_RED);   // Filled rectangle
board.rootmaker.lcd->drawRect(x, y, width, height, TFT_WHITE); // Rectangle outline
board.rootmaker.lcd->fillScreen(TFT_BLACK);                     // Fill the entire screen
board.rootmaker.lcd->clearDisplay();                             // Clear the screen
```

#### Read Touch Input

```cpp
uint16_t x, y;
if (board.rootmaker.lcd->getTouch(&x, &y)) {
    // Touch detected; x and y are the touch coordinates
    Serial.printf("Touch: (%d, %d)\n", x, y);
}
```

#### Play GIF Animations

Use the AnimatedGIF library to play GIF animations:

```cpp
#include <AnimatedGIF.h>

AnimatedGIF gif;

gif.begin(BIG_ENDIAN_PIXELS);
if (gif.open((uint8_t *)gifData, gifSize, GIFDraw)) {
    while (gif.playFrame(true, NULL)) {
        yield();
    }
    gif.close();
}
```

---

### RGB LED

RootMaker includes a WS2812B RGB LED driven by the Adafruit_NeoPixel library.

#### Initialization

```cpp
board.rootmaker.begin(false, true, false, false, false); // Enable LED only
```

#### Set Colors

```cpp
// Set the pixel color (pixel index, R, G, B)
board.rootmaker.led.strip.setPixelColor(0, 255, 0, 0);  // Red
board.rootmaker.led.strip.show();  // Update the display
```

#### Rainbow Cycle Effect

```cpp
void rainbowCycle(int wait) {
    for (int j = 0; j < 256 * 5; j++) {
        for (int i = 0; i < board.rootmaker.led.strip.numPixels(); i++) {
            board.rootmaker.led.strip.setPixelColor(i, Wheel(((i * 256 / board.rootmaker.led.strip.numPixels()) + j) & 255));
        }
        board.rootmaker.led.strip.show();
        delay(wait);
    }
}

uint32_t Wheel(byte wheelPos) {
    if (wheelPos < 85) {
        return board.rootmaker.led.strip.Color(wheelPos * 3, 255 - wheelPos * 3, 0);
    } else if (wheelPos < 170) {
        wheelPos -= 85;
        return board.rootmaker.led.strip.Color(255 - wheelPos * 3, 0, wheelPos * 3);
    } else {
        wheelPos -= 170;
        return board.rootmaker.led.strip.Color(0, wheelPos * 3, 255 - wheelPos * 3);
    }
}
```

---

### Button

RootMaker has an onboard user button (GPIO0) supporting short press, long press, double click, and hold detection.

#### Initialization

```cpp
board.rootmaker.begin(false, false, false, true, false); // Enable button only
```

#### Detect Events

```cpp
Button_event_t event = board.rootmaker.btn.update();

switch (event) {
    case BTN_EVENT_SHORT_PRESS:
        Serial.println("Short press");
        break;
    case BTN_EVENT_LONG_PRESS:
        Serial.println("Long press");
        break;
    case BTN_EVENT_DOUBLE_CLICK:
        Serial.println("Double click");
        break;
    case BTN_EVENT_LONG_PRESSING:
        Serial.println("Holding");
        break;
    default:
        break;
}
```

| Event | Description |
|:---:|:---|
| BTN_EVENT_SHORT_PRESS | Released after a short press |
| BTN_EVENT_LONG_PRESS | Released after a long press |
| BTN_EVENT_DOUBLE_CLICK | Two quick clicks |
| BTN_EVENT_LONG_PRESSING | Button held down (repeatedly triggered) |

---

### LIS2DWTR Accelerometer

RootMaker includes a LIS2DWTR 3-axis accelerometer for orientation detection, motion recognition, and related applications.

#### Initialization

```cpp
board.rootmaker.begin(false, false, true, false, false); // Enable sensor only
```

#### Read Acceleration Data

```cpp
int32_t accelerometer[3];
board.rootmaker.lis2dwtr->read_acceleration(accelerometer, 3);

Serial.printf("X: %d\tY: %d\tZ: %d\n", 
              accelerometer[0], accelerometer[1], accelerometer[2]);
```

### Battery Management

RootMaker includes a PY32 battery management chip supporting battery voltage readings, battery percentage, charging status detection, and more.

#### Initialization

```cpp
board.rootmaker.begin(false, false, false, false, true); // Enable battery management only
```

#### Check Connection Status

```cpp
if (board.rootmaker.bat.isConnected()) {
    Serial.println("Battery management chip connected");
    
    uint16_t version = board.rootmaker.bat.getVersion();
    Serial.printf("Firmware version: v%d.%d\n", version >> 8, version & 0xFF);
}
```

#### Read Battery Information

```cpp
// Read battery voltage (mV)
uint32_t voltage = board.rootmaker.bat.getVoltage();
Serial.printf("Battery voltage: %ld mV\n", voltage);

// Read battery percentage (0-100)
uint8_t level = board.rootmaker.bat.getBatteryLevel();
Serial.printf("Battery level: %d%%\n", level);
```

#### Detect Charging Status

```cpp
ChargingStatus_t status = board.rootmaker.bat.getChargingStatus();

switch (status) {
    case CHARGING_STATUS_NOT_CHARGING:
        Serial.println("Not charging");
        break;
    case CHARGING_STATUS_CHARGING:
        Serial.println("Charging");
        break;
    case CHARGING_STATUS_COMPLETE:
        Serial.println("Fully charged");
        break;
}
```

#### Power Button Configuration

```cpp
uint16_t wakeup_time = board.rootmaker.bat.getKeyWakeupTime();    // Wake-up time (ms)
uint16_t shutdown_time = board.rootmaker.bat.getKeyShutdownTime(); // Shutdown time (ms)
```

## Complete Example: Touchscreen Interaction

The following example demonstrates LCD touchscreen interaction: a red block appears on screen and moves to a random new position when tapped.

```cpp
#include "Ryzobee.h"

Ryzobee board(RYZOBEE_ROOTMAKER);

#define CUBE_WIDTH 40
long randNumber_x = (SCREEN_WIDTH - CUBE_WIDTH) / 2;
long randNumber_y = (SCREEN_WIDTH - CUBE_WIDTH) / 2;

void setup(void)
{
    Serial.begin(115200);
    randomSeed(analogRead(A0));

    board.rootmaker.begin(true, false, false, false, false);
    board.rootmaker.lcd->setBrightness(255);
    board.rootmaker.lcd->setTextSize(2);
    board.rootmaker.lcd->fillScreen(TFT_BLACK);
    board.rootmaker.lcd->fillRect(randNumber_x, randNumber_y, CUBE_WIDTH, CUBE_WIDTH, 0xf800);
    board.rootmaker.lcd->drawString("Please click the cube", 60, 230);
}

void loop(void)
{
    uint16_t x, y;
    if (board.rootmaker.lcd->getTouch(&x, &y)) {
        if (x >= randNumber_x && x <= randNumber_x + CUBE_WIDTH &&
            y >= randNumber_y && y <= randNumber_y + CUBE_WIDTH) {
            randNumber_x = random(0, SCREEN_WIDTH - CUBE_WIDTH);
            randNumber_y = random(0, SCREEN_WIDTH - CUBE_WIDTH);
            board.rootmaker.lcd->clearDisplay();
            board.rootmaker.lcd->fillRect(randNumber_x, randNumber_y, CUBE_WIDTH, CUBE_WIDTH, 0xf800);
            board.rootmaker.lcd->drawString("Please click the cube", 60, 230);
        }
    }
}
```

## Frequently Asked Questions

### Compilation error: Ryzobee.h not found?

Check the following:

1. Make sure the Ryzobee_arduino_esp32 library is in the Arduino libraries directory.
2. Make sure all dependencies are installed and meet the minimum version requirements.
3. Make sure ESP32S3 Dev Module is selected in the Arduino IDE.

### The LCD is blank?

Possible causes include:

- LCD was not enabled in `begin()` (the first parameter must be `true`).
- `setBrightness()` was not called to set the backlight brightness.
- The wrong board model is selected.

### Touch input does not respond?

Suggestions:

- Make sure the LCD is initialized correctly.
- Check that touch coordinates are within 0-239.
- Try cycling the power.

### Accelerometer readings are zero?

Possible causes include:

- The sensor was not enabled in `begin()` (SensorEnable must be `true`).
- There is an I2C bus conflict; check whether another device uses the same address.

### Battery level cannot be read?

Suggestions:

- Make sure `board.rootmaker.bat.isConnected()` returns `true`.
- Check that the PY32 chip is soldered correctly.
- Make sure BatteryEnable is enabled in `begin()`.
