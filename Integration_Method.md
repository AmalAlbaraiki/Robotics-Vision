# 🔗 Integration Method — ESP32 + Flask + ChatGPT

## 1. Overview
The integration connects hardware (ESP32 + HuskyLens) with software (Flask + ChatGPT).  
When a person is detected, the ESP32 notifies the server, which generates a reply using ChatGPT and displays it visually.

---

## 2. System Components
| Component | Role |
|------------|------|
| ESP32 | Sends detection signals via HTTP |
| HuskyLens | Detects human presence |
| Flask | Acts as middleware between ESP32 and ChatGPT |
| ChatGPT API | Generates conversational responses |
| Python UI | Displays visual “eyes” and text |

---

## 3. Communication Flow
HuskyLens → ESP32 (UART)
ESP32 → Flask Server (HTTP POST)
Flask → ChatGPT API (REST Request)
ChatGPT → Flask → Eye Display



---

## 4. Implementation Steps
1. **ESP32 Setup**
   - Connect HuskyLens using UART.
   - Send detection flag to Flask server using Wi-Fi.

2. **Flask API**
   - Receive detection event at endpoint `/detect`.
   - Call `chatbot_service.py` to handle ChatGPT request.
   - Return response to front-end visual system.

3. **ChatGPT Integration**
   - Uses `openai_handler.py` for requests.
   - Parses response and sends it to the display.

4. **Visual Feedback**
   - Python UI (`eye_display.py`) shows awake/sleeping eyes.
   - Displays current conversation text in real-time.

---

## 5. Error Handling
- **Network Retry:** Retries if ChatGPT API call fails.
- **Timeout:** Flask server avoids hanging on slow responses.
- **Logging:** SQLite records each interaction and detection.

--
# 📚 References

1. OpenAI API Documentation — https://platform.openai.com/docs  
2. HuskyLens Official Documentation — https://www.dfrobot.com/product-1922.html  
3. ESP32 Official Docs — https://docs.espressif.com/projects/esp-idf/en/latest/esp32/  
4. Flask Web Framework — https://flask.palletsprojects.com/  
5. SQLite Documentation — https://www.sqlite.org/docs.html  
6. Research Papers on Human-Robot Interaction (HRI)
7. Additional Tutorials & Open Source AI Guides from GitHub and YouTube
