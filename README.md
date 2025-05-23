# Arduino Automatic Pet Feeder

This project is an automatic pet feeder built using an Arduino, an RTC (Real-Time Clock) module, an LCD display, and a servo motor. It allows you to schedule two automatic feeding times for your pet.

## Features

* **Automatic Feeding:** Dispenses pet food at two preset times using a servo motor.
* **Real-Time Clock:** Keeps accurate time to ensure precise feeding schedules.
* **LCD Display:** Shows current time, date, and navigation menus.
* **Button Control:** Easy-to-use buttons to set feeding times and check status.
* **Alerts:** Buzzer and LED activate when food is dispensed.

## Components Needed

* Arduino Uno
* DS3231 RTC Module
* I2C LCD Display (20x4)
* Servo Motor
* 4 Push Buttons
* Buzzer
* LED

## Setup

1.  **Wire up the components:** Connect the RTC, LCD, servo, buttons, buzzer, and LED to your Arduino as shown in the circuit diagram (refer to the code for pin definitions).
2.  **Install Libraries:** Install `DS3231`, `LiquidCrystal_I2C`, and `Servo` libraries in your Arduino IDE.
3.  **Upload Code:** Open the `.ino` file in Arduino IDE, select your board and port, then upload.

## How to Use

* The LCD will show the current time and date.
* Use the buttons to navigate menus:
    * **"OK" button:** Enter the "Set Waktu Makan" (Set Feeding Time) menu.
        * Choose "Waktu makan 1" or "Waktu makan 2".
        * Use "Kiri" to adjust minutes, "Kanan" to adjust hours.
        * Press "Keluar" to save.
    * **"Kanan" button (from Home screen):** View "Sisa Waktu" (Remaining Time) until the next feeding.
    * **"Kiri" button (from Home screen):** Check "Cek Status" (Status) of the feeding schedules.
    * **"Keluar" button:** Exit current menu and return to the home screen.
* At the scheduled feeding time, the servo will dispense food, and the buzzer/LED will activate.

---
