
---

# 🤖 Line Following Bot 🚀  

🏆 **Competition-Winning Project Sponsored by IEEE** 🏅  

This project is a high-performance **line-following robot** built with Arduino, IR sensors, and a motor control system. Using **PID control**, it smoothly follows a path with precision and agility. This bot won **1st place** at a prestigious competition sponsored by IEEE! 🌟  

---

## ✨ Features  

- 🎯 **PID Control**: Ensures accurate and smooth path-following.  
- 🚦 **Real-Time Sensor Feedback**: IR sensors detect and respond to the line dynamically.  
- ⚡ **Optimized Design**: Compact and efficient for competitive scenarios.  

---

## 🛠️ Components  

- **🖥️ Microcontroller**: Arduino (CH430 driver installed)  
- **🌈 IR Sensors**: Line detection via contrast sensing.  
- **🔧 Motors**: DC motors controlled using an H-bridge driver.  
- **🏎️ Chassis**: Lightweight and competition-ready.  
- **🔋 Power Source**: Battery-powered for portability.  

---

## 🔌 Circuit Diagram  

*![Diagram](/CircuitDiagram.jpeg)
*  

---

## 💻 Code  

The bot is powered by an efficient Arduino program implementing **PID control** for precise movement. Here's a snippet:  

```c
// PID constants
float Kp = 1.2, Ki = 0.01, Kd = 0.5;
float error = 0, lastError = 0, integral = 0;

// Sensors and motor pins
#define LEFT_SENSOR A0
#define RIGHT_SENSOR A1
#define LEFT_MOTOR 5
#define RIGHT_MOTOR 6

void loop() {
  int leftSensor = analogRead(LEFT_SENSOR);
  int rightSensor = analogRead(RIGHT_SENSOR);

  error = leftSensor - rightSensor;
  integral += error;
  float derivative = error - lastError;

  float correction = (Kp * error) + (Ki * integral) + (Kd * derivative);

  analogWrite(LEFT_MOTOR, constrain(200 - correction, 0, 255));
  analogWrite(RIGHT_MOTOR, constrain(200 + correction, 0, 255));

  lastError = error;
}
```

---

## 🏅 Competition Details  

- **Event Name**: [Insert competition name]  
- **Sponsor**: IEEE ✨  
- **Date**: [Insert date]  
- **Outcome**: 🏆 **Winners!**  
- **Highlights**: Showcased superior performance, smooth navigation, and precise turns.  

---

## 📸 Gallery  

- 📷 **Bot in Action**: *(Upload pictures of the bot, team, and competition setup.)*  
- 🏅 **Certificate of Achievement**: *(Upload your winning certificate as proof.)*  

---

## 🚀 How to Run  

1. 🔌 **Set Up Hardware**: Assemble the bot using the circuit diagram.  
2. 💾 **Upload Code**: Use Arduino IDE to upload the program.  
3. 🛤️ **Place on Track**: Position the bot on a black line over a white surface.  
4. 🚀 **Start and Watch**: Turn on the bot and watch it follow the line seamlessly!  

---

## 🌟 Future Upgrades  

- 🚧 Add obstacle detection using ultrasonic sensors.  
- ⚡ Further optimize PID constants for faster response.  
- 📶 Integrate wireless communication for remote control.  

---

