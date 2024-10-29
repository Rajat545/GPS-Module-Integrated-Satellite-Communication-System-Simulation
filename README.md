# GPS-Module-Integrated-Satellite-Communication-System-Simulation
Developed a system using a GPS module (NEO-6M) and Arduino or ESP32 to simulate satellite communication and tracking. Integrated GPS data with simulation software to visualize satellite navigation systems like Fleet Broadband and Sat-C

## Project Overview
This project simulates a satellite communication system integrated with a GPS module using an ESP32. It demonstrates collecting GPS data, processing it, and simulating transmission to a satellite system

## Components Required
- GPS Module (e.g., Neo-6M)
- ESP32 Development Board
- Jumper Wires
- Breadboard (optional for connections)
- USB Cable (for ESP32 power and programming)
- Computer (with Arduino IDE installed)

## Hardware Setup

### Step 1: Connecting the GPS Module to the ESP32

**Power Connections:**
- GPS Module VCC: Connect to the 3.3V pin on the ESP32.
- GPS Module GND: Connect to the GND pin on the ESP32.

**Data Connections:**
- GPS Module TX: Connect to RX on the ESP32 (e.g., GPIO 16).
- GPS Module RX: Connect to TX on the ESP32 (e.g., GPIO 17).

*Note:* Verify that you are using the correct GPIO pins for TX and RX on your ESP32. You may need to adjust these if your ESP32 model has different serial pin mappings.

### Step 2: Power the Setup
Plug the ESP32 into your computer or a USB power source using a USB cable. This will provide power to both the ESP32 and the GPS module.
![circuit_image (2)](https://github.com/user-attachments/assets/ff50da71-7b64-4e3c-aea3-f01be7aaceb0)


## Software Setup

### Step 1: Install Arduino IDE (if not already installed)
- Download and install the Arduino IDE 
- Open the Arduino IDE.

### Step 2: Install ESP32 Board Support
- Go to `File > Preferences`.
- In the **Additional Board Manager URLs** field, paste:
- Go to `Tools > Board > Board Manager`, search for **ESP32**, and click **Install**.

### Step 3: Install TinyGPSPlus Library for GPS
- Go to `Sketch > Include Library > Manage Libraries`.
- Search for **TinyGPSPlus** and click **Install** to add it to your Arduino IDE.

# GPS Module-Integrated Satellite Communication System with Google Maps API Integration

## Step 1: Set Up Google Cloud Console

### 1.1 Enable Google Maps API
1. Go to [Google Cloud Console](https://console.cloud.google.com/).
2. Create a new project (or use an existing one).
3. Navigate to **APIs & Services > Library**.
4. Search for **Maps JavaScript API** and **Geocoding API**, then enable them both.

### 1.2 Obtain API Key
1. Go to **APIs & Services > Credentials**.
2. Click **Create Credentials > API Key**.
3. Copy the generated **API Key** to use in your ESP32 project.

## Step 2: Install Required Libraries

To parse JSON responses, install the **ArduinoJson** library.
1. Go to **Sketch > Include Library > Manage Libraries** in the Arduino IDE.
2. Search for **ArduinoJson** and install it.

## Step 3: Configure GPS Code with Google Maps API

1. Open the Arduino IDE and enter the following code.
2. Replace `"YOUR_GOOGLE_MAPS_API_KEY"` with
3. Replace `"WIFI USERNAME AND PASSWORD"`.


### Step 4: Upload the code to ESP32

## Usage Instructions
1. **Upload the code** to your ESP32 using the Arduino IDE.
2. **Open the Serial Monitor** in Arduino IDE to retrieve the ESP32’s IP address.
3. **Open a web browser** and enter the IP address. This will display a Google Map with the ESP32’s real-time GPS location data.

