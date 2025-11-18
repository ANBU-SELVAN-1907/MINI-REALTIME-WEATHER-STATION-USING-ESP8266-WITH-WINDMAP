# MINI-REALTIME-WEATHER-STATION-USING-ESP8266-WITH-WINDMAP
A compact IoT weather station using ESP8266 with real-time temperature, humidity, and air-quality monitoring (MQ135), 1-second live updates, OLED display support, and a modern mobile-friendly web dashboard. Includes MQ135 D0 indicator, live charts, and an embedded Windy.com weather map with free Open-Meteo forecast.
_____________________________________________________by Anbu-Selvan____________________________________________________

# 🌦️ ESP8266 Weather Station  
### MQ135 Air Quality • DHT/BME Sensor • Windy Map • OLED (SSH1106) • Live Charts • Forecast

A complete IoT Weather Monitoring System built using **ESP8266**, providing real-time weather, air quality, OLED display output, and a modern web dashboard with live charts and an embedded **Windy** weather map.

This project includes:

- 📡 **Live Web Dashboard (1-second updates)**
- 🌡️ Temperature (°C)
- 💧 Humidity (%)
- 🫁 Air Quality (MQ135 A0 + D0)
- ▒ Live D0 “Good/Medium/Bad Air” bar
- 📊 Real-time chart (Temperature, Humidity, AQ Index)
- 🖥️ **1.96" SSH1106 OLED** (U8G2 library)
- 🌍 Embedded **Windy.com** map
- 🔮 **7-day Weather Forecast (Open-Meteo API)**
- 🚀 Mobile-friendly responsive UI
- 🌐 API endpoint (`/data`)
- 🔌 Auto-update every **1 second**
- 📦 Single-file HTML dashboard (served from ESP)

---
## outputs:
![20251118_205459](https://github.com/user-attachments/assets/026e8342-8f9d-430b-970b-5de6ad0564cd)

![20251118_205418](https://github.com/user-attachments/assets/8b37e61e-3163-4127-9d72-dd1cdcc2acbb)

![20251118_205433](https://github.com/user-attachments/assets/6a21443d-959a-47f7-b508-67afdcafcd98)

<img width="1915" height="1031" alt="Screenshot 2025-11-18 210612" src="https://github.com/user-attachments/assets/2cf72198-ad8d-4814-a5f6-c8bdc9a3a70f" />

<img width="1917" height="1027" alt="image" src="https://github.com/user-attachments/assets/aa888b37-bdec-406b-ad0b-64203f8d29cf" />


## 🚀 Features

### ⭐ Real-Time Dashboard
The ESP8266 hosts a dynamic UI showing:
- Temperature (°C)
- Humidity (%)
- Air Quality Index (calculated from MQ135)
- Digital D0 level → Good / Moderate / Bad
- Status indicator (Live / Disconnected)
- Real-time chart (auto-refresh every second)
- Last update timestamp
- IP address
- Weather forecast data
- Embedded Windy weather radar map

### ⭐ MQ135 Air Quality Sensor
- **A0 → Analog AQ Index**
- **D0 → Digital threshold alert**
- Easy calibration using onboard trimmer

Displays:
- Fresh Air  
- Moderate  
- Poor Air  
- Hazardous (if D0 triggered)

### ⭐ OLED Display (1.96" SSH1106)
Uses **U8G2** library to show:
- Boot animation
- WiFi IP
- Temperature + Humidity
- MQ135 Raw + AQ Index
- D0 Warning Indicator
- Weather Condition Text
- Refresh every 1 second

### ⭐ 7-Day Weather Forecast  
Using **Open-Meteo** (100% free, no key):
- Current temperature  
- Apparent temperature  
- Wind speed  
- Daily high/low  
- Rain probability  
- Sunrise / Sunset  

### ⭐ Embedded Windy Map
Using iframe:
https://embed.windy.com/embed2.html


Shows:
- Radar  
- Clouds  
- Temperature  
- Wind  
- Precipitation  

---

## 📡 API Endpoint `/data`

Returns sensor data + forecast:

```json
{
  "temp": 28.5,
  "hum": 67,
  "mq_raw": 414,
  "mq_index": 88,
  "d0": 0,
  "ip": "192.168.1.20",
  "forecast": { ... },
  "timestamp": 123456789
}


