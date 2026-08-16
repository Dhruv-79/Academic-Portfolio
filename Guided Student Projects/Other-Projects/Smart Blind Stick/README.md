# 🦯 Smart Blind Stick

## 📌 Project Overview

The **Smart Blind Stick** is an IoT-enabled assistive device designed to improve the safety, mobility, and emergency-response capabilities of visually impaired users.

The system uses **NodeMCU (ESP8266)** as its central controller and integrates ultrasonic sensors for obstacle detection, GPS for location tracking, audio and vibration feedback for alerts, and the Blynk IoT platform for emergency communication. :contentReference[oaicite:0]{index=0}

## 🎯 Objectives

- To detect obstacles in real time.
- To provide audio and tactile alerts.
- To monitor the user's location using GPS.
- To provide an emergency SOS mechanism.
- To transmit the user's location to caregivers.
- To develop a low-cost assistive technology solution.
- To improve independent navigation and user safety.

## ⚙️ Key Features

- 🚧 Dual ultrasonic obstacle detection
- 📍 GPS location tracking
- 🔊 Audio alerts
- 📳 Vibration-based alerts
- 🆘 Emergency SOS button
- ☁️ Blynk IoT connectivity
- 📱 Caregiver notifications
- 🗺️ Google Maps location sharing
- 🔋 Portable battery-powered operation

## 🏗️ System Architecture

```text
              Smart Blind Stick
                     │
              NodeMCU ESP8266
                     │
       ┌─────────────┼─────────────┐
       ▼             ▼             ▼
 Ultrasonic       GPS Module    SOS Button
  Sensors             │             │
       │              │             │
       ▼              ▼             ▼
Obstacle          Location      Emergency
Detection          Data          Trigger
       │              │             │
       └───────┬──────┘             │
               ▼                    ▼
        Audio + Vibration       Blynk IoT
             Alerts                 │
                                    ▼
                              Caregiver Alert
