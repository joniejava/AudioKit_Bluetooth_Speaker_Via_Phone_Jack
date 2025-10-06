# AudioKit_Bluetooth_Speaker_Via_Phone_Jack

🎶 **ESP32 AudioKit v2.2 Bluetooth Audio Sink**  
This project turns the ESP32 AudioKit board into a Bluetooth speaker that receives audio from your phone and plays it through the onboard DAC and 3.5 mm headphone jack.

## 🔧 Features
- Acts as a **Bluetooth A2DP sink**
- Outputs clear audio via the **3.5 mm jack**
- Based on **AudioTools** and **ESP32-A2DP** libraries
- Simple setup — no SD card or network required
- Tested with iPhone and Android devices

## 🧠 Requirements
- ESP32 AudioKit v2.2 board  
- Latest Arduino IDE  
- Libraries:
  - `audio-tools` (v1.2.0 or newer)
  - `ESP32-A2DP` (v1.8.7 or newer)

## ⚙️ How to Use
1. Flash the sketch to your ESP32 AudioKit.  
2. Power up — it will advertise as **"AudioKit_ESP32"**.  
3. Pair your phone and play audio — it will stream through the 3.5 mm output.

---

🧑‍💻 _Created and tested by John Hulme_  
_Repository initialized from verified working base_

