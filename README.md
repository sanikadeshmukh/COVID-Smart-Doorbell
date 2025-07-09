## 🔧 Components Used

- Arduino UNO
- LCD Display 16x2
- Ultrasonic Sensor (HC-SR04)
- Analog Temperature Sensor (TMP36 or LM35)
- Red LED
- Buzzer (Piezoelectric)
- Potentiometer (for LCD contrast)
- Jumper wires and Breadboard

---

## ⚙️ Functionality

- **Distance Measurement**: Uses ultrasonic sensor to measure how close a person is.
- **Temperature Reading**: Uses analog sensor to measure body temperature in Fahrenheit.
- **Alert Mechanism**:
  - If **temperature ≥ 99.6°F** and **distance < 50 cm**, the system:
    - Lights up the red LED
    - Triggers a buzzer
  - Otherwise:
    - Turns off the LED and buzzer
- **LCD Display**: Continuously shows real-time temperature and distance.

---

## 📑 Code Summary

- `analogRead(A0)`: Reads voltage from the temperature sensor.
- `pulseIn(pingPin, HIGH)`: Measures ultrasonic echo time to calculate distance.
- `tone(8, 440, 200)`: Activates buzzer at 440 Hz if alert condition met.
- `lcd.print()`: Displays temperature and distance on the LCD.

---

## 🖥️ How to Use

1. Connect all components as per the circuit diagram (see project report or use TinkerCAD).
2. Upload the code to Arduino UNO via the Arduino IDE.
3. Power the Arduino.
4. Place your hand or body in front of the ultrasonic sensor.
5. Observe the temperature and distance on the LCD. If threshold conditions are met, alerts will trigger.

---

## ✅ Conditions for Trigger

```
if (temperature ≥ 99.6°F && distance < 50 cm):
    Trigger LED and Buzzer
else:
    No alert
```

---

## 📂 File Structure

- `face_mask_temp_detector.ino` — Main Arduino sketch file
- `Final SNL report.pdf` — Complete project report with literature review, diagrams, and references

---

## 📚 References

- TinkerCAD simulations for buzzer, temperature, and ultrasonic sensors
- Arduino documentation: https://www.arduino.cc
- Face mask detection (for full implementation including OpenCV, TensorFlow – see report)

---

## 🙋 Authors

- **Sanika Deshmukh**
