# Voice Operated Wheelchair

A low-cost, Arduino-based wheelchair control system that allows users to move the wheelchair using simple voice commands via Bluetooth. This project improves mobility for individuals with limited hand movement by replacing physical controls with voice-activated navigation.

---

## 🚀 Features
- Fully voice-controlled movement through a smartphone app  
- Bluetooth-based communication with the microcontroller  
- Supports: **forward**, **backward**, **left**, **right**, **stop**  
- Motor driver integration for precise wheel control  
- Works on simple and inexpensive hardware components  
- Easily extendable for additional commands or sensors  

---

## 📌 How It Works
1. The user speaks a command into a smartphone app.  
2. The command is converted to text and sent to the wheelchair via Bluetooth.  
3. The onboard microcontroller (Arduino) receives the command.  
4. Based on the command, the motors are activated in the required direction.  

**Example:**  
- \`*forward#\` → both motors rotate forward  
- \`*left#\` → right motor moves while the left motor pauses  
- \`*stop#\` → all motors turn off  

The logic is implemented in the Arduino code using digital motor control pins.

---

## 🧩 System Architecture
**Core Components**
- Arduino/microcontroller  
- HC-05/06 Bluetooth module  
- 12V DC motors  
- Motor driver circuitry  
- Battery (12V recommended)  
- Voice recognition smartphone app  

**Control Flow**
\`\`\`
Voice Command → Smartphone → Bluetooth → Arduino → Motor Driver → Motors
\`\`\`

---

## 🛠️ Hardware Requirements
- Arduino UNO / AT89C52-based controller  
- HC-05 Bluetooth module  
- 12V DC motors (4)  
- Motor driver module (e.g., L298N/H-Bridge setup)  
- Battery (12V lead-acid or similar)  
- Basic chassis / wheelchair base  
- Wires, connectors, and mounting hardware  

Optional:
- Solar charging module  
- Joystick (for fallback manual control)  

---

## 📡 Bluetooth Command Format
The system uses specific formatted commands:

| Command    | Description              |
|------------|--------------------------|
| \`*forward#\` | Move forward              |
| \`*back#\`    | Move backward             |
| \`*left#\`    | Turn left                 |
| \`*right#\`   | Turn right                |
| \`*stop#\`    | Stop all movement         |

---

## 💻 Arduino Code
The complete working code is included in the file \`bt-voice.txt\`.  
It sets up:
- Bluetooth serial communication  
- Motor movement functions  
- Command parsing logic  
- Direction control for each motor  

### Motor Pin Mapping
| Pin | Function |
|-----|----------|
| 3   | Motor A Direction 1 |
| 4   | Motor A Direction 2 |
| 5   | Motor B Direction 1 |
| 6   | Motor B Direction 2 |

Each movement function uses combinations of HIGH/LOW values to rotate the motors accordingly.

---

## ⚙️ Installation & Setup
1. Upload the Arduino code to the board.  
2. Connect the Bluetooth module to RX/TX pins.  
3. Wire the motor driver outputs to the motors.  
4. Pair the smartphone with the HC-05 module.  
5. Use any Bluetooth terminal / voice-control app to send commands.  

---

## 🔮 Future Enhancements
This system can be extended with:
- Multi-language voice commands  
- Obstacle detection using ultrasonic sensors  
- Auto-charging system using motion energy  
- Customizable voice commands  
- Smartphone app with GUI and safety alerts  

---

## 📄 License
This project is open-source. You may modify and adapt it based on your requirements.
