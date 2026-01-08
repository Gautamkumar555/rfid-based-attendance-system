# RFID Based Smart Attendance System 📡

An IoT-based attendance management system using **NodeMCU ESP8266**, **MFRC522 RFID reader**, and **Google Sheets** for real-time cloud storage.

---

## 📖 Description

The RFID Based Smart Attendance System automates the process of recording attendance using RFID technology and cloud services. Each user is assigned an RFID card with a unique ID stored in **Block 4** of the card. When scanned, the system reads the card data and uploads the attendance details (date, time, and card ID) directly to **Google Sheets** using Google Apps Script over Wi-Fi.

This project reduces manual effort, eliminates attendance errors, and provides secure, real-time access to attendance data.

---

## ✨ Features

- Automatic attendance recording  
- Real-time Google Sheets integration  
- RFID data reading from Block 4  
- Wi-Fi enabled using ESP8266  
- Paperless and error-free system  
- Low-cost and scalable design  

---

## 🛠️ Hardware Requirements

- NodeMCU ESP8266  
- MFRC522 RFID Reader (13.56 MHz)  
- RFID Cards / Tags (13.56 MHz)  
- Breadboard  
- Jumper Wires  
- Micro USB Cable  
- Wi-Fi Internet Connection  

---

## 💻 Software Requirements

- Arduino IDE  
- ESP8266 Board Package  
- MFRC522 Library  
- Google Sheets  
- Google Apps Script  

---

## 🔌 Circuit Connections

| MFRC522 | NodeMCU ESP8266 |
|--------|----------------|
| SDA    | D2             |
| SCK    | D5             |
| MOSI   | D7             |
| MISO   | D6             |
| RST    | D1             |
| GND    | GND            |
| 3.3V   | 3.3V           |

⚠️ **Note:** Use only **3.3V** power for the MFRC522 module.

---

## 📁 Project Structure

RFID-Attendance-System/ ├── sending_to_sheets_with_ap.zip ├── README.md ├── circuit_diagram.png └── screenshots/

---

## 📦 Installation

1. Install **Arduino IDE**
2. Add **ESP8266 Board Package** via Boards Manager
3. Install required libraries:
   - MFRC522
   - ESP8266WiFi
4. Connect the hardware as per the circuit diagram

---

## ⚙️ Google Sheets Setup

1. Create a new Google Sheet  
2. Add the following headers in Row 1:

Date | Time | Card ID | Name | Status

3. Open **Extensions → Apps Script**
4. Paste the provided Apps Script code
5. Deploy as a **Web App**
6. Set access to **Anyone**
7. Copy the generated Web App URL

---

## 🧩 Code Configuration

Update the following fields in the Arduino sketch:

```cpp
const char* ssid = "YOUR_WIFI_SSID";
const char* password = "YOUR_WIFI_PASSWORD";
String GOOGLE_SCRIPT_URL = "YOUR_WEB_APP_URL";

```
---

🔄 Working Flow

1. RFID card is scanned


2. MFRC522 reads data from Block 4


3. NodeMCU connects to Wi-Fi


4. Data is sent to Google Apps Script


5. Attendance is stored in Google Sheets




---

📊 Sample Output

Date	Time	Card ID	Name	Status

05-01-2026	10:30 AM	A1B2C3D4	Gautam	Present



---

✅ Advantages

Fast and reliable

Real-time cloud storage

Easy to use

No paperwork

Accurate attendance tracking



---

❌ Limitations

Requires active internet connection

Limited RFID reading range

RFID card loss possible



---

🚀 Future Improvements

Face recognition integration

Mobile application support

Email/SMS notifications

Firebase or database backend

Admin dashboard



---

🏫 Applications

Schools and colleges

Offices

Libraries

Laboratories

Secure access systems



---

📝 Conclusion

This project demonstrates an effective integration of RFID technology with IoT and cloud services. The system provides a smart, efficient, and scalable solution for attendance management, suitable for educational institutions and workplaces.


---

👨‍💻 Author

Gautam Kumar


---

📜 License

This project is open-source and intended for educational purposes only.
