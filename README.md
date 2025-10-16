# 🤖 Robotics Vision

A smart interactive robot that detects and interacts with humans using AI and computer vision.  
Developed as a **graduation project** at Yanbu Industrial College, this robot integrates **HuskyLens**, **ESP32**, and **ChatGPT** to simulate human-like conversation and emotional eye expressions.

---

## 📌 Overview
The project recognizes human presence and responds with facial expressions and voice-based interactions.  
It combines **AI conversation**, **face detection**, and **real-time eye animations**, creating a natural human-robot communication experience.

---

## 🎯 Objectives
- Detect human presence using **HuskyLens**.  
- Enable AI conversation via **ChatGPT API**.  
- Display expressive animated eyes that react to user interaction.  
- Build a modular and scalable architecture for future development.

---

## ⚙️ Methodology & Design
- The robot uses **ESP32** microcontroller for data handling and communication.  
- **Python (Flask)** powers the animated eyes interface and AI logic.  
- **HuskyLens** provides real-time face detection and tracking.  
- **ChatGPT API** manages conversation and dialogue generation.  
- Data communication between **ESP32** and the **Python app** is handled via **UART**.

---

## 🧠 Tools & Technologies
| Category | Tools Used |
|-----------|-------------|
| Programming Languages | Python, C++ |
| AI & APIs | OpenAI ChatGPT API |
| Hardware | ESP32, HuskyLens AI Camera |
| Frameworks | Flask, PyGame |
| Development Tools | Visual Studio, Arduino IDE |

---

## 🔍 Implementation Flow
1. **HuskyLens** detects human faces and sends a signal to **ESP32**.  
2. **ESP32** transmits detection status to the **Python GUI** through **UART**.  
3. The **Python app** triggers eye animations and initializes AI conversation using **ChatGPT**.  
4. Eye expressions dynamically change based on human interaction.  

---

## 🧩 Project Structure
Robotics-Vision/
├─ esp32/
│ └─ huskylens_esp32.ino # Arduino sketch (ESP32)
├─ server/
│ ├─ app.py # Flask API server
│ ├─ openai_handler.py # Handles ChatGPT API requests
│ ├─ db.py # SQLite helper
│ └─ requirements.txt
├─ ui/
│ ├─ eye_display.py # Animated eyes display (PyGame)
│ └─ assets/ # Images, icons, or GIFs for eyes
├─ docs/
│ ├─ wiring_diagram.png
│ └─ demo.gif # Short demo preview
├─ .env.example
├─ .gitignore
├─ README.md
└─ LICENSEد

---

## 📈 Results
- The robot successfully detects human presence.  
- Responds with voice and expressive eye animations.  
- Works efficiently in real time with smooth synchronization.  

---

## 🚀 Future Improvements
- Add voice recognition input.  
- Integrate emotional expressions and natural movement.  
- Support mobile or web-based remote control.  
- Use MQTT or socket networking for multi-device communication.  
- Deploy on **Raspberry Pi** for full embedded performance.

---

 🧑‍💻 Developer
**Amal Mohammed Albarakati**  
Yanbu Industrial College – Computer Science (Software Engineering Path)  
Graduation Project supervised by **Basma Aldahlan**

---

## 🪄 Installation

# Clone the repository
git clone https://github.com/<your-username>/Robotics-Vision.git
cd Robotics-Vision

# Install dependencies
pip install -r requirements.txt

# Run the application
python app.py
🧠 Demo
<img width="894" height="269" alt="لقطة شاشة 2025-10-15 213601" src="https://github.com/user-attachments/assets/189f3e6d-b292-4abc-8d35-55071e481071" />
<img width="688" height="310" alt="لقطة شاشة 2025-10-15 213539" src="https://github.com/user-attachments/assets/46f7a609-325d-4f4b-acd7-ea8b85700069" />
<img width="947" height="848" alt="image" src="https://github.com/user-attachments/assets/56b6e271-00f9-4e3e-8958-ddaa9990d049" />

📜 License
This project is for educational and research purposes.
© 2025 Amal Mohammed Albarakati. All rights reserved.


