---

# 🕹️ Reaction-Test-OLED-Display

### **Description**

An Arduino-based reaction timer game that uses an SSD1306 128x32 OLED display, LEDs, buzzer, and buttons to test how fast you can respond after the “Go!” signal.

![](circuit_image.png) 
![](558212761_2705025093162460_1664318836026426263_n.jpg)
![](558880183_2705025163162453_976367281857834950_n.jpg)
---

## ⚙️ **Features**

* “Ready, Set, Go!” LED sequence (**White → Yellow → Green → Red**)
* Reaction time measured precisely in milliseconds
* OLED display feedback for each stage
* Idle **background music** (BGM) while waiting for player input
* **False start prevention** — the player must wait for “Go!”
* Clean reset with dedicated button
* Compact display interface using 128x32 OLED

---

## 🧰 **Technologies Used**

* **Arduino UNO R3** (microcontroller)
* **OLED SSD1306 128x32 I2C display**
* **Passive buzzer** (for tones and BGM)
* **LEDs** (White, Yellow, Green, Red)
* **Momentary push buttons** (Start / Reset)
* **C++ / Arduino IDE**

---

## 🚀 Getting Started

### 1. **Circuit Setup**

| Component    | Arduino Pin |
| ------------ | ----------- |
| White LED    | D2          |
| Yellow LED   | D3          |
| Green LED    | D4          |
| Red LED      | D5          |
| Buzzer       | D6          |
| Game Button  | D7          |
| Reset Button | D8          |
| OLED SDA     | A4          |
| OLED SCL     | A5          |
| OLED VCC     | 5V          |
| OLED GND     | GND         |

Use **330Ω resistors** for all LEDs.

---

### 2. **Library Installation**

In Arduino IDE:

```
Sketch → Include Library → Manage Libraries…
Search and install:
- Adafruit SSD1306
- Adafruit GFX Library
```

### 3. **Upload the Code**

Upload the `.ino` file to your Arduino UNO.
Ensure your board and COM port are correctly set.
---

## 🕹️ **Usage**

* When idle, the system plays soft background tones.
* Press **Start** to begin — the LEDs light up in sequence (“Ready, Set, Go!”).
* When the **Red LED** lights up and “GO!” appears on screen, press the **Start button** as fast as you can.
* The OLED displays your **reaction time** in milliseconds.
* Press **Reset** to return to idle mode.

---

## 🗂️ **Project Structure**

```
reaction-test-oled-display/
├── reaction-test-oled-display.ino
├── README.md
└── libraries/
    ├── Adafruit_GFX
    └── Adafruit_SSD1306
```

---

## 📦 **Packaging for Distribution**

* Include source code `.ino` and wiring guide.
* Provide dependency list and library versions.
* Optionally bundle preconfigured Arduino IDE sketch folder.

---

## 🔮 **Future Enhancements**

* Add **high-score memory** using EEPROM
* Implement **multi-player mode**
* Display **average reaction time** after multiple tries
* Include **animated graphics** or countdown on OLED
* Adjustable BGM or mute option

---

## 🧾 **Changelog**

**v1.1 – Current**

* Fixed LED order (White → Yellow → Green → Red)
* Added idle background music using passive buzzer
* Improved reaction time accuracy
* Synced buzzer and OLED messages

**v1.0 – Initial Release**

* Basic reaction test with OLED display
* Simple LED countdown and buzzer tone

---

## 💻 **System Requirements**

* Arduino IDE 2.x
* Arduino UNO or compatible board
* 5V power supply or USB connection

---

## 🧩 **Troubleshooting**

| Issue               | Possible Cause              | Solution                               |
| ------------------- | --------------------------- | -------------------------------------- |
| OLED not displaying | Wrong I2C address           | Verify I2C (use 0x3C)                  |
| LEDs always on      | No resistor or wiring short | Use 330Ω resistors per LED             |
| Buzzer not playing  | Using active buzzer         | Replace with passive buzzer            |
| Button unresponsive | Wrong pin or missing GND    | Check button wiring and pull-up config |

---

## 🙏 **Acknowledgements**

* **Adafruit** for OLED and GFX libraries
* **Arduino Community** for open hardware support
* Inspired by classic reaction timer arcade games
* **Sir’s Project Design** and concept direction
* app.cirkitdesigner.com
* Nooby 
* Firelink
* SBBC PC
* Rita's PC
* To my dog and cat

---

## ⚖️ **License**

This project is licensed under the **MIT License** — free for modification, sharing, and educational use.

---

Would you like me to include a **circuit diagram image section** (placeholder line for now) so you can upload your wiring diagram later to the GitHub page?
