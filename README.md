#  IR Sensor-Based Tachometer using Arduino Nano

This project is a **digital tachometer** built using an **Infrared (IR) sensor** and an **Arduino Nano** to calculate the **Revolutions Per Minute (RPM)** of a rotating vehicle wheel or shaft. It is a low-cost, efficient, and contactless method of measuring RPM, ideal for DIY and academic projects.

---

## 🔧 Components Used

* Arduino Nano
* IR Obstacle Sensor Module
* Reflective surface (white tape or sticker on wheel/shaft)
* OLED/16x2 LCD Display (optional, for real-time output)
* Jumper wires
* Breadboard or PCB

---

## ⚙️ How It Works

1. **IR Sensor Setup**:
   The IR sensor emits infrared light. When a **white reflective surface** (e.g., tape) passes in front of the sensor, the IR light reflects back and is detected. A black or non-reflective surface does not reflect the IR light, so the sensor only "triggers" when it sees the reflective tape.

2. **Pulse Counting**:
   The Arduino Nano monitors the **digital output** of the IR sensor. Each time the reflective surface passes by the sensor, a **pulse** is detected. Each pulse corresponds to **one rotation** of the wheel/shaft.

3. **Time Measurement**:
   The Arduino measures the time between pulses and calculates how many pulses occur in one minute, which gives the **RPM**.

4. **Formula Used**:

   ```cpp
   RPM = (pulse_count / time_interval_in_seconds) * 60;
   ```

5. **Display**:
   The RPM value is updated and displayed on a serial monitor or OLED/LCD screen in real-time.

---

## 🛠️ Applications

* Automotive RPM monitoring
* Motor speed measurement
* Robotics and automation
* Educational electronics projects
