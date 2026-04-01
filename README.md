# 📱 ESP32 IoT Control App

## 📌 Overview
This project demonstrates a simple IoT solution using an ESP32 microcontroller and an Android application to monitor and control devices in real time.

The system allows users to:
- Read digital input from a push-button
- Control LED output
- Monitor device status
- Apply embedded systems and mobile development concepts in practice

---

## 🧠 Technologies Used
- ESP32
- Arduino IDE
- C/C++
- Android Studio
- Kotlin
- GPIO Digital Input/Output

---

## ⚙️ System Architecture
Android App ↔ ESP32 ↔ LED / Push-button

---

## 🔌 Hardware Components
- ESP32
- LED
- Push-button
- Resistors
- Breadboard
- Jumper wires

---

## 💡 Features
- Digital input reading
- Digital output control
- LED activation based on button state
- Simple real-time embedded logic

---

## 📂 Project Structure

esp32-iot-control-app/
├── README.md
├── esp32-code/
│ └── main.ino
└── android-app/
└── MainActivity.kt

---

## 🔧 ESP32 Code

```cpp
const int LEDPIN = 12;
const int BOTAO_1 = 22;

int VALOR_B1 = 0;

void setup() {
  pinMode(LEDPIN, OUTPUT);
  pinMode(BOTAO_1, INPUT);
  Serial.begin(115200);
}

void loop() {
  VALOR_B1 = digitalRead(BOTAO_1);

  if (VALOR_B1 == 1) {
    digitalWrite(LEDPIN, HIGH);
  } else {
    digitalWrite(LEDPIN, LOW);
  }

  delay(500);
}
📱 Android App

The Android app provides a simple interface to interact with the ESP32 system, allowing monitoring and control of connected devices.
.

📸 Demonstration

(Add screenshots or photos of the circuit and app interface here)

📊 Results
Successful real-time control
Stable communication
Improved interaction with physical devices
🚀 Future Improvements
Cloud integration (Firebase)
Data logging
Multiple device control
UI/UX improvements
👩‍💻 Author

Michele Noronha
Agile Project & Delivery Manager | SAP S/4HANA Cloud | IoT & Software Development

📄 License

This project is for academic purposes.

✔ Developed as part of an academic IoT project
✔ Focus on real-world application and automation
