# 🎧 AudioKit Bluetooth Speaker via Phone Jack  
**Transform your ESP32 AudioKit v2.2 into a Bluetooth receiver that plays audio through the 3.5 mm jack.**  
Built with love, resilience, and a rediscovered passion for creativity through technology.

---

## 💡 Overview

This project turns an **ESP32 AudioKit v2.2** board into a **Bluetooth speaker**.  
It receives audio wirelessly from your phone and outputs sound via the onboard **3.5 mm audio jack** or **RCA ports**.

What started as a troubleshooting experiment became something much deeper —  
a symbol of rebuilding, rediscovery, and reclaiming a lifelong dream.

---

## ❤️ The Story Behind the Code

> *“This isn’t just a project — it’s a turning point in my life.”*

After years of hard physical work — from **gardening** to **mechanic**, **scaffolding**, **roofing**, **plastering**, and **joinery** —  
I was forced to stop when **heart failure** changed everything.  

During recovery, I lost almost everything that gave my life structure.  
I went through a **manipulative breakup**, **financial fraud**, and worst of all, my **two kids were taken** from me through lies and greed.  
For two years, I cried every day — missing them, questioning everything.  

But then something inside me shifted.  
I rediscovered the kid who once sat in front of an **Amstrad CPC464**, writing **a 1000-line BASIC card game**,  
the boy who loved code and imagination.  

Now, at **49**, I’ve found my new path — learning **C++**, **Python**, **Bash**, and **Git**.  
Building circuits, fixing hardware, and bringing sound to life again.  

This project — this **AudioKit Bluetooth Speaker** — is a symbol that not every day is a bad day.  
It’s proof that rebuilding is possible.  
It’s a reminder that **you can always start again**.

One day, my kids will know the truth.  
And they’ll see that their dad didn’t give up — he *rebuilt himself from scratch*.

---

## ⚙️ Hardware Setup

| Component | Description |
|------------|-------------|
| **Board** | ESP32 AudioKit v2.2 (AI Thinker) |
| **Audio Output** | 3.5 mm jack or RCA out |
| **Power Supply** | 5 V USB-C or barrel jack |
| **Bluetooth Role** | Audio Sink (receives audio from phone) |

---

## 🔧 Arduino Configuration

**Board Manager:**  
`ESP32 by Espressif Systems @ v2.0.14`

**Libraries Used:**
```text
ESP32-A2DP @ 1.8.7
AudioTools @ 1.2.0

