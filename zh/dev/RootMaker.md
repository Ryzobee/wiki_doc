<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Dev/img/rootmaker_main_image.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

RootMaker 是 Ryzobee 系列的首款开发板，基于 ESP32-S3 平台，集成 LCD 屏幕、触摸、RGB LED、加速度传感器、按键和电池管理等丰富外设，适用于 3D 打印互动作品和创意电子项目。

<div style="border-left: 6px solid #ff6a00;background: #fff7ed;padding: 10px 16px; border-radius: 0px;">
  <h3 class="toc-header" style="margin-top: 0px; color:#FFA00;"><a href="https://github.com/Ryzobee" class="toc-anchor"></a>📘<a style="color: #FF6A00; text-decoration: none;"> Rootmaker产品规格</a></h3>
  <p style="margin-bottom: 10px;">
  如果您还没有了解RootMaker产品，请看RootMaker产品Wiki页面
  </p>
<div style="text-align: center;"><a href="/zh/root/rootmaker" target="_blank" style="display: inline-block; padding: 4px 25px; background: #FF6A00; color: rgb(255, 255, 255); border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none; border-radius: 50px; font-weight: bold; text-decoration: none; transition: transform 0.2s; margin: 5px; box-shadow: none;">
    点击跳转到RootMaker产品Wiki页面 →
    </a></div></div>

## 硬件规格

| 项目 | 说明 |
|:---:|:---|
| 主控 | ESP32-S3 |
| Flash | 16MB (QIO 80MHz) |
| PSRAM | 2MB QSPI PSRAM |
| LCD | SPI / ST7789, 240×240 |
| 触摸 | CST816T 电容触摸 |
| LED | WS2812B RGB LED |
| 传感器 | LIS2DWTR 3轴加速度计 |
| 按键 | 板载用户按键 (GPIO0) |
| 电池管理 | TP4054 充电 + PY32 电量管理 |
| 扩展接口 | 4路 RS-Port (I2C) |

## Arduino IDE 配置

| 项目 | 配置 |
|:---:|:---:|
| 开发板 | ESP32S3 Dev Module |
| Flash Mode | QIO 80MHz |
| Flash Size | 16MB |
| PSRAM | 2MB |

## 快速开始

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
    // 你的代码
}
```

### begin() 参数说明

`begin()` 方法支持按需启用各模块：

```cpp
void begin(bool LCDEnable      = false, 
           bool LEDEnable      = true, 
           bool SensorEnable   = true, 
           bool ButtonEnable   = true,
           bool BatteryEnable  = true);
```

| 参数 | 默认值 | 说明 |
|:---:|:---:|:---|
| LCDEnable | false | 是否启用 LCD 屏幕和触摸 |
| LEDEnable | true | 是否启用 WS2812B RGB LED |
| SensorEnable | true | 是否启用 LIS2DWTR 加速度计 |
| ButtonEnable | true | 是否启用板载按键 |
| BatteryEnable | true | 是否启用电池管理 |

> **注意**：LCD 默认关闭，需要使用屏幕时请手动启用。

## 示例程序

Ryzobee 库内置了多个示例程序，涵盖 RootMaker 开发板的所有板载外设功能。

### 在 Arduino IDE 中打开示例

1. 打开 Arduino IDE
2. 点击菜单 **文件 > 示例**
3. 滚动找到 **Ryzobee** 分类
4. 选择需要的示例程序即可打开

### 可用示例列表

| 示例 | 功能说明 |
|:---:|:---|
| battery | 电池电量监测，LED 颜色指示电量，屏幕显示电压和充电状态 |
| btn | 按键事件检测（短按 / 长按 / 双击 / 长按保持） |
| gif | GIF 动画播放，按键切换不同动画 |
| i2c_scan | 扫描 4 路 RS-Port 扩展接口上的 I2C 设备 |
| led | RGB LED 彩虹循环效果 |
| lis2dwtr | LIS2DWTR 加速度传感器读取 XYZ 轴数据 |
| screen | 触摸屏交互，点击移动方块小游戏 |

### 使用步骤

1. 通过 **文件 > 示例 > Ryzobee** 打开示例程序
2. 在 **工具 > 开发板** 中选择 `ESP32S3 Dev Module`
4. 用 USB 线连接 RootMaker 开发板
5. 在 **工具 > 端口** 中选择对应的串口
6. 点击上传按钮烧录程序

> **提示**：建议从 `led` 或 `btn` 示例开始，验证开发环境是否配置正确，再尝试更复杂的示例。

## 外设操作指南

### LCD 屏幕

RootMaker 板载一块 240×240 分辨率的 ST7789 SPI LCD，并集成 CST816T 电容触摸芯片。LCD 模块基于 LovyanGFX 图形库封装。

#### 初始化

```cpp
board.rootmaker.begin(true, false, false, false, false); // 仅启用 LCD

board.rootmaker.lcd->setBrightness(255);  // 设置背光亮度 (0-255)
board.rootmaker.lcd->fillScreen(TFT_BLACK);  // 清屏
```

#### 文字显示

```cpp
board.rootmaker.lcd->setTextSize(2);
board.rootmaker.lcd->setTextColor(TFT_WHITE, TFT_BLACK);
board.rootmaker.lcd->drawString("Hello Ryzobee!", 60, 120);
```

#### 图形绘制

```cpp
board.rootmaker.lcd->fillRect(x, y, width, height, TFT_RED);   // 填充矩形
board.rootmaker.lcd->drawRect(x, y, width, height, TFT_WHITE); // 矩形边框
board.rootmaker.lcd->fillScreen(TFT_BLACK);                     // 全屏填充
board.rootmaker.lcd->clearDisplay();                             // 清屏
```

#### 触摸读取

```cpp
uint16_t x, y;
if (board.rootmaker.lcd->getTouch(&x, &y)) {
    // 检测到触摸，x 和 y 为触摸坐标
    Serial.printf("Touch: (%d, %d)\n", x, y);
}
```

#### GIF 动画播放

配合 AnimatedGIF 库可播放 GIF 动画：

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

RootMaker 板载一颗 WS2812B RGB LED，通过 Adafruit_NeoPixel 库驱动。

#### 初始化

```cpp
board.rootmaker.begin(false, true, false, false, false); // 仅启用 LED
```

#### 设置颜色

```cpp
// 设置像素颜色 (像素编号, R, G, B)
board.rootmaker.led.strip.setPixelColor(0, 255, 0, 0);  // 红色
board.rootmaker.led.strip.show();  // 刷新显示
```

#### 彩虹循环效果

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

### 按键

RootMaker 板载一个用户按键（GPIO0），支持短按、长按、双击和长按保持事件检测。

#### 初始化

```cpp
board.rootmaker.begin(false, false, false, true, false); // 仅启用按键
```

#### 事件检测

```cpp
Button_event_t event = board.rootmaker.btn.update();

switch (event) {
    case BTN_EVENT_SHORT_PRESS:
        Serial.println("短按");
        break;
    case BTN_EVENT_LONG_PRESS:
        Serial.println("长按");
        break;
    case BTN_EVENT_DOUBLE_CLICK:
        Serial.println("双击");
        break;
    case BTN_EVENT_LONG_PRESSING:
        Serial.println("长按保持中");
        break;
    default:
        break;
}
```

| 事件 | 说明 |
|:---:|:---|
| BTN_EVENT_SHORT_PRESS | 短按释放 |
| BTN_EVENT_LONG_PRESS | 长按释放 |
| BTN_EVENT_DOUBLE_CLICK | 快速双击 |
| BTN_EVENT_LONG_PRESSING | 长按保持中（持续触发） |

---

### LIS2DWTR 加速度传感器

RootMaker 板载 LIS2DWTR 三轴加速度计，可用于姿态检测、运动识别等场景。

#### 初始化

```cpp
board.rootmaker.begin(false, false, true, false, false); // 仅启用传感器
```

#### 读取加速度数据

```cpp
int32_t accelerometer[3];
board.rootmaker.lis2dwtr->read_acceleration(accelerometer, 3);

Serial.printf("X: %d\tY: %d\tZ: %d\n", 
              accelerometer[0], accelerometer[1], accelerometer[2]);
```

### 电池管理

RootMaker 内置 PY32 电池管理芯片，支持电池电压读取、电量百分比、充电状态检测等功能。

#### 初始化

```cpp
board.rootmaker.begin(false, false, false, false, true); // 仅启用电池管理
```

#### 检测连接状态

```cpp
if (board.rootmaker.bat.isConnected()) {
    Serial.println("电池管理芯片已连接");
    
    uint16_t version = board.rootmaker.bat.getVersion();
    Serial.printf("固件版本: v%d.%d\n", version >> 8, version & 0xFF);
}
```

#### 读取电池信息

```cpp
// 读取电池电压 (mV)
uint32_t voltage = board.rootmaker.bat.getVoltage();
Serial.printf("电池电压: %ld mV\n", voltage);

// 读取电量百分比 (0-100)
uint8_t level = board.rootmaker.bat.getBatteryLevel();
Serial.printf("电池电量: %d%%\n", level);
```

#### 充电状态检测

```cpp
ChargingStatus_t status = board.rootmaker.bat.getChargingStatus();

switch (status) {
    case CHARGING_STATUS_NOT_CHARGING:
        Serial.println("未充电");
        break;
    case CHARGING_STATUS_CHARGING:
        Serial.println("充电中");
        break;
    case CHARGING_STATUS_COMPLETE:
        Serial.println("充电完成");
        break;
}
```

#### 电源键配置

```cpp
uint16_t wakeup_time = board.rootmaker.bat.getKeyWakeupTime();    // 唤醒时间 (ms)
uint16_t shutdown_time = board.rootmaker.bat.getKeyShutdownTime(); // 关机时间 (ms)
```

## 综合示例：触摸屏交互

以下示例演示了 LCD 触摸屏交互功能——在屏幕上显示一个红色方块，用户点击方块后方块随机移动到新位置：

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

## 常见问题

### 编译报错找不到 Ryzobee.h？

请检查以下内容：

1. 确认已将 Ryzobee_arduino_esp32 库放置在 Arduino libraries 目录下。
2. 确认所有依赖库已正确安装且版本满足最低要求。
3. 确认 Arduino IDE 开发板选择为 ESP32S3 Dev Module。

### LCD 屏幕无显示？

可能原因包括：

- `begin()` 时未启用 LCD（第一个参数需设为 `true`）。
- 未调用 `setBrightness()` 设置背光亮度。
- 开发板型号选择错误。

### 触摸无响应？

建议：

- 确认 LCD 已正确初始化。
- 检查触摸坐标范围是否在 0-239 之内。
- 尝试重新上电。

### 加速度计读取为0？

可能原因包括：

- `begin()` 时未启用传感器（SensorEnable 需设为 `true`）。
- I2C 总线冲突，检查是否有其他设备占用相同地址。

### 电池电量无法读取？

建议：

- 确认 `board.rootmaker.bat.isConnected()` 返回 `true`。
- 检查 PY32 芯片是否正确焊接。
- 确认 `begin()` 时已启用 BatteryEnable。
