# ARGUS GUARD

### Safety in Seconds

## Team Details

**Team Name:** TECHPULSE

**Domain:** Internet of Things (IoT)

### Team Members
- REVANT D
- ADVAIT DN
- KESAVA SAI RR
- GOUTHAM SIVA
- MONISH KS
- KISHORE S

---

# Problem Statement

Industrial workplaces such as construction sites and manufacturing facilities face significant risks from worker injuries, fires, hazardous environments, and delayed emergency response.

Current safety systems mainly focus on detection and alerting, leaving emergency response, evacuation guidance, and coordination to manual decision-making. This can increase response time and put lives at risk.

---

# Solution

ARGUS GUARD is a smart industrial emergency response ecosystem that combines worker monitoring, environmental hazard detection, dynamic evacuation guidance, and emergency response coordination into a single connected platform.

The system consists of:

- A wearable safety device for workers
- Smart environmental monitoring nodes
- A centralized command dashboard

ARGUS GUARD helps detect emergencies, verify incidents, guide workers to safety, and assist emergency services in responding more effectively.

---

# Features

### Worker Wearable
- Motion-based fall detection
- False alarm reduction using verification period
- Manual emergency cancellation
- Audible alerts through buzzer
- Visual alerts using LED matrix

### Smart Corridor
- Fire detection
- Smoke and gas detection
- Temperature monitoring
- Dynamic evacuation guidance
- Smart LED exit indicators

### Command Center
- Real-time incident monitoring
- Worker status tracking
- Hazard monitoring
- Emergency response coordination
- Emergency escalation support

---

# Complete Tech Stack

## Hardware
- Arduino UNO R4 WiFi
- ESP32 / ESP8266
- MPU6050 Accelerometer & Gyroscope
- HC-SR501 PIR Sensor
- MQ-2 Gas Sensor
- DHT11 / DHT22 Temperature Sensor
- IR Flame Sensor
- WS2812B LED Strip
- Push Button
- Active Buzzer

## Software
- Arduino C++
- MQTT Communication
- Adafruit IO Dashboard
- IFTTT Automation

## Communication
- WiFi
- MQTT Protocol

---

# System Architecture Diagram

```text
                    ┌───────────────────┐
                    │  Worker Wearable  │
                    │                   │
                    │ MPU6050           │
                    │ PIR Sensor        │
                    │ Button            │
                    │ Buzzer            │
                    │ LED Matrix        │
                    └─────────┬─────────┘
                              │
                              │ MQTT
                              ▼
                    ┌───────────────────┐
                    │    Adafruit IO    │
                    │  Cloud Platform   │
                    └─────────┬─────────┘
                              │
               ┌──────────────┴──────────────┐
               ▼                             ▼
    ┌───────────────────┐       ┌───────────────────┐
    │ Smart Corridor    │       │ Command Center    │
    │                   │       │ Dashboard         │
    │ Flame Sensor      │       │ Incident Monitor  │
    │ MQ2 Sensor        │       │ Status Tracking   │
    │ DHT Sensor        │       │ Coordination      │
    │ LED Strip         │       │ Escalation        │
    └───────────────────┘       └───────────────────┘
```

---

# Detailed Workflow

## Scenario 1: Worker Injury

```text
Worker Fall Detected
          ↓
15 Second Verification Period
          ↓
Movement Detected OR Button Pressed?
          ↓
YES → Alarm Cancelled

NO
          ↓
Critical Alert Generated
          ↓
Dashboard Notification
          ↓
Emergency Response Initiated
```

## Scenario 2: Fire Emergency

```text
Fire / Smoke Detected
          ↓
Hazard Zone Identified
          ↓
Alert Sent To Dashboard
          ↓
Safe Route Determined
          ↓
LED Guidance Activated
          ↓
Workers Evacuated Safely
```

---

# Folder Structure

```text
ARGUS-GUARD/

├── wearable/
│   └── wearable.ino

├── smart-corridor/
│   └── corridor.ino

├── dashboard/

├── diagrams/

├── images/

└── README.md
```

---

# Installation & Usage Guide

## Worker Wearable

1. Connect MPU6050 sensor.
2. Connect PIR sensor.
3. Connect push button.
4. Connect active buzzer.
5. Upload firmware to Arduino UNO R4 WiFi.
6. Configure WiFi credentials.
7. Configure Adafruit IO credentials.

## Smart Corridor

1. Connect flame sensor.
2. Connect MQ-2 sensor.
3. Connect DHT sensor.
4. Connect WS2812B LED strip.
5. Upload firmware to ESP32/ESP8266.
6. Connect device to Adafruit IO.

## Dashboard

1. Create Adafruit IO dashboard.
2. Configure MQTT feeds.
3. Monitor worker and hazard status in real time.

---

# Hardware Components

| Component | Purpose |
|------------|------------|
| Arduino UNO R4 WiFi | Worker wearable controller |
| ESP32 / ESP8266 | Smart corridor controller |
| MPU6050 | Motion and fall detection |
| PIR Sensor | Movement verification |
| Push Button | Alarm cancellation |
| Active Buzzer | Audible alerts |
| IR Flame Sensor | Fire detection |
| MQ-2 | Smoke and gas detection |
| DHT11 / DHT22 | Temperature monitoring |
| WS2812B LED Strip | Evacuation guidance |

---

# Hardware Workflow

```text
MPU6050 Motion Event
          ↓
Verification Period
          ↓
Alert Generated
          ↓
MQTT Transmission
          ↓
Dashboard Notification

Flame / Gas / Temperature
          ↓
Hazard Detection
          ↓
Safe Route Guidance
          ↓
LED Evacuation Indicators
```

### Circuit / Wiring Diagram
*Insert circuit diagram image here.*

---

# Security Measures

- Password-protected WiFi connectivity
- MQTT-based communication
- Cloud authentication through Adafruit IO
- Local alerts continue functioning even during network interruption

---

# Testing & Performance

### Tested Functions

- Fall detection
- Alarm cancellation workflow
- MQTT communication
- Dashboard notifications
- Fire detection simulation
- Hazard alert generation
- Evacuation guidance workflow

### Performance Goals

- Real-time alert transmission
- Reduced false alarms
- Faster emergency awareness
- Improved evacuation coordination

---

# Challenges Faced

- Reducing false positives in fall detection
- Integrating multiple IoT nodes
- Ensuring reliable MQTT communication
- Designing an effective emergency workflow
- Coordinating wearable and environmental systems

---

# Future Scope

- AI-assisted injury assessment
- Advanced evacuation route optimization
- Mobile application integration
- Smart city emergency integration
- Enhanced emergency service coordination
- Large-scale industrial deployment

---

# Demo Screenshots / Video

### Hardware Prototype
*Insert hardware images here.*

### Dashboard
*Insert dashboard screenshots here.*

### Demo Video
*Insert video link here.*

---

# References

1. Arduino Documentation
2. Adafruit IO Documentation
3. MQTT Documentation
4. MPU6050 Datasheet
5. ESP32 Documentation
6. OSHA Workplace Safety Guidelines

---

## Tagline

**ARGUS GUARD — Safety in Seconds**
