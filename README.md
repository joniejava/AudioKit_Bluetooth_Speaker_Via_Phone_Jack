# AudioKit_Bluetooth_Speaker_Via_Phone_Jack

### 🎧 Description
This project turns the ESP32 AudioKit v2.2 board into a Bluetooth speaker.  
When paired with a phone, any audio streamed over Bluetooth is output via the 3.5mm headphone jack.

### 🧩 Hardware
- ESP32 AudioKit v2.2
- Standard 3.5mm headphones or speakers

### 🛠️ Software
- Arduino IDE 2.x
- Libraries:
  - `audio-tools` (latest)
  - `ESP32-A2DP`

### 🔧 Usage
1. Upload the sketch `AudioKit_BT_Sink_Working_Base.ino`
2. Check the serial monitor:
   - Should display “✅ Advertising as 'AudioKit_ESP32'”
3. On your phone, pair with **AudioKit_ESP32**
4. Play music — sound comes through the 3.5mm jack 🎶

### 🧠 Notes
- Tested on ESP32 AudioKit v2.2
- Works as a Bluetooth sink (not transmitter)
- Volume controlled from the connected phone

---
