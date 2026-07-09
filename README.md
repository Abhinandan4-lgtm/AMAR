# 🤖 AMAR - AI Medical Assistance Robot

AMAR (AI Medical Assistance Robot) is an AI-powered healthcare assistant designed to automate medicine dispensing, improve medication adherence, and provide remote monitoring for elderly individuals and patients. The system combines embedded hardware, artificial intelligence, IoT, and web technologies into a single healthcare platform.

---

# 📌 Problem Statement

Medication non-adherence is one of the major challenges faced by elderly patients, individuals with chronic illnesses, and people who require continuous medication. Missed or incorrect doses can lead to serious health complications.

Existing reminder systems often provide only alarms and lack intelligent assistance, remote monitoring, emergency support, and automated dispensing capabilities.

AMAR addresses these challenges by providing an intelligent medication management system capable of automating medicine dispensing, monitoring patient activity, assisting through voice interaction, and notifying caregivers during emergencies.

---

# 🎯 Objectives

The primary objectives of AMAR are:

- Automate medicine dispensing based on scheduled timings.
- Improve medication adherence and patient safety.
- Provide AI-powered voice assistance for patient interaction.
- Enable remote monitoring through a web dashboard.
- Generate emergency alerts during critical situations.
- Maintain medication history and activity logs.
- Create an easy-to-use system suitable for elderly users.

---

# ⚙️ Methodology

AMAR follows a modular layered architecture.

1. The guardian configures patient details and medicine schedules through the web dashboard.

2. The backend server stores patient information and dispensing schedules in the database.

3. The Raspberry Pi continuously monitors the schedule.

4. At the scheduled time, the Raspberry Pi activates the dispensing mechanism using servo motors.

5. Voice reminders are generated using Text-to-Speech while patient responses are captured using Speech-to-Text.

6. Dispensing activities are logged and synchronized with the web dashboard.

7. During emergencies, the GSM module sends alerts and the Pi Camera starts live streaming for remote monitoring.

---

# 🏗️ System Architecture

```
Guardian Dashboard
        │
 REST API + WebSocket
        │
 Flask Backend Server
        │
 ┌──────────────┬──────────────┬─────────────┐
 │              │              │
Database      AI Module     Hardware Layer
 │              │              │
 └──────── Raspberry Pi ───────┘
        │
 ┌──────┼─────────┬──────────┬──────────┐
 │      │         │          │
Servo  Camera    USB Mic   GSM Module
        │
 Bluetooth Speaker
```

---

# ✨ Features

- Automated medicine dispensing
- AI voice assistant
- Speech-to-Text
- Text-to-Speech
- Patient management
- Medicine scheduling
- Emergency alert system
- Live video streaming
- Guardian dashboard
- Activity logging
- AI-powered schedule summaries
- Remote monitoring

---

# 🛠️ Hardware Components

- Raspberry Pi 3A+
- Raspberry Pi Camera Module
- USB Microphone
- Bluetooth Speaker
- Servo Motors
- SIM800L GSM Module
- Push Button
- Power Supply

---

# 💻 Software Stack

### Backend

- Python
- Flask
- Flask-SocketIO
- APScheduler

### Frontend

- HTML5
- CSS3
- JavaScript
- Bootstrap

### AI

- Google Gemini API

### Database

- SQLite
- JSON

### Communication

- REST API
- WebSockets

---

# 🚀 Software Setup

## Step 1

Clone the repository.

```bash
git clone https://github.com/yourusername/AMAR.git

cd AMAR
```

---

## Step 2

Install dependencies.

```bash
pip install -r requirements.txt
```

---

## Step 3

Configure Raspberry Pi.

```bash
sudo raspi-config
```

Enable:

- Camera
- SSH
- Serial Port
- I2C

Reboot the Raspberry Pi.

---

## Step 4

Run the backend server.

```bash
python3 app.py
```

---

## Step 5

Find the Raspberry Pi IP address.

```bash
hostname -I
```

---

## Step 6

Open the dashboard in your browser.

```
http://<RaspberryPi-IP>:5000
```

---

# 🔌 Hardware Connections

| Component | Connection |
|------------|------------|
| Rotation Servo | GPIO17 |
| Dispense Servo | GPIO27 |
| Emergency Button | GPIO2 |
| GSM TX | GPIO15 |
| GSM RX | GPIO14 |
| Pi Camera | CSI Port |
| USB Microphone | USB Port |
| Bluetooth Speaker | Bluetooth |

---

# 📂 Project Structure

```
AMAR
│
├── backend/
├── frontend/
├── hardware/
├── database/
├── documentation/
├── requirements.txt
└── README.md
```

---

# 🚀 Future Enhancements

- Mobile application
- Offline AI assistant
- Face recognition
- Health sensor integration
- Cloud synchronization
- Voice authentication
- Multi-patient management

---

# 👨‍💻 Developer

**Abhinandan A S**

Bachelor of Engineering

Electrical and Electronics Engineering

---
