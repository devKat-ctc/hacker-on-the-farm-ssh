# 🌾 Hacker on the Farm

Inspired by the song ["The Hacker on the Farm"](https://open.spotify.com/track/715HQIg2dWEeN1dRkkFHAm?si=fa8991b43f0f4c8c), this guide helps you learn how to use serial terminals, CAN logs, and embedded devices like ESP32, Raspberry Pi Pico, and more.

🧠 Pre-Work Briefing: Gear Up for the Mission

Welcome, Operative.

Before the main event kicks off, we’ve got some warm-up exercises to get your mind in the right gear. Whether you’re a fresh recruit or a seasoned tractor hacker, there’s something here for you. All of these are optional!

🛠️ No Hardware? No Worries.
We get it — not everyone has a lab bench at home. If you don’t have access to hardware yet, you’ll get your tools(ESP32) at the event. But if you can't wait you can also use the software below for hardware simulation. 

These missions can be completed with just your brain — but we recommend doing a few by hand before using software tools to help decode the data. Not only will it make your life easier, it’ll also help you get familiar with the tools and concepts we’ll be working with in person.

🔐 The mission starts now. Choose your challenge and dive in.

‍🌾🔧 Happy hacking! ‍🌾🔧
---

## 📚 Table of Contents
- [🔓 Challenges](#challenges)
- [🛠️ Software](#software)
- [📋 Recommended Tutorials](#Recommended-Tutorials)

---

## 🔓 Challenges 

### 1. 🧑‍🌾🕵️‍♂️🔐 “The Ag Cipher”

[🔗 File](./logs/ag_cipher.log)
This one’s for the new operatives. Your mission: crack a friendly message that’s been scrambled into machine-speak. Along the way, you’ll pick up some essential skills:

Converting hex to ASCII
Reading a message frame
Making sense of little vs. big endian formats
No stress, no rush — just get comfy with the bytes.

### 2. 📡📶🧩 “Signals in the Noise”

[🔗 File](./logs/signals.txt)
For those ready to dive deeper. This challenge drops you into the middle of a digital traffic jam. Your goal: make sense of a data stream from an unknown source. This one sets the tone for what’s coming at the event — decoding, pattern recognition, and protocol intuition.

Try to answer the following questions:

What was the top speed in whole miles per hour of the truck during this time period?
What was the lowest engine speed in RPM during this time period?
Did the driver have the cruise control set during this time?
Did the driver press the service brake pedal during this time?
How many different controller applications are broadcasting data on the J1939 network during this time?
How many parameter group numbers are on the network at this time?
What is the CAN bus load during this time?


### 3. 🥖🗺️🌾 “Breadcrumbs in the Field”

Every operation has players, tools, and tactics. Your job is to figure out what — and who — you’re walking into.

This OSINT-style challenge tasks you with uncovering:

Clues about who might be at the event (organizers, speakers, tech partners, aliases…)
What tools or platforms might be in play (hint: think hardware, protocols, open-source kits)
Any strategic insights hiding in social posts, GitHub repos, blog write-ups, or DNS records
If it’s public, it’s fair game. Operatives who know what’s coming are one step ahead.

---
#### 🧑‍🦰 Seth's OSINT Tips

OSINT (Open Source Intelligence) is a fancy term for "research." Skilled hackers don't just know how to use Google or other search engines to find anything publicly available about a person, company, or device, but also know how to tweak their search to show things you'd usually never find publicly. We won't be going too in-depth on how to do this, but we at least want to point you in the right direction for how to perform OSINT on a piece of hardware. We'll also be providing you with the basics of how a tractor’s tech stack works, but learning how we learn about the devices that show up on our desks is crucial to the work you'll be doing the week of CTC and the work out on the field. 
1) When you have a device that you don't know about, you can start off simply by Googling its identifiers, like its Serial Number, IMEI, etc.) Odds are you'll find the device descriptions from the manufacturer right away.
2) If that doesn't work but you're able to find an FCC ID, you've hit a jackpot already. Any FCC-registered devices require manufacturers to submit these devices with precise descriptions, user manuals, datasheets, pretty much everything you need.​
3) The last step you can take is opening it up and looking at the components inside. You can use the same Google approach with the labels found on the microchips and identifying codes on the circuits.
---

### ⭐ Bonus Challenge: “Logging the Harvest”

 Welcome to the digital farm, field agent. The sensors are planted, the signals are ripe, and your job is to log the entire yield — from root to shell. Take the given files and write the file to a serial terminal and then save the serial output into a new file.

This combined mission teaches you how to:
* Read and write to a serial device (think: moisture/temp sensors, or… encrypted livestock chatter 👀)
* Write that stream to a file using Python, creating a clean harvest log
* Simultaneously log your terminal activity — every command you plow through, every bug you weed out, and every insight you grow
You’ll gain hands-on skills with:
* pyserial for serial port communication
* Python file I/O for writing structured logs
* Tools like script, tee, or custom logging scripts to track your terminal session
🌾 Extra rows in your row crop:
* Add timestamps to each data entry for traceability
* Format logs like a digital field journal (e.g., CSV, JSON, Markdown tables)
* Bonus if your script can detect and “weed out” duplicate or noisy data!

Good hackers document their harvest. Great ones timestamp the rainfall, tag the pests, and leave a clean field for whoever comes next. 🌱

This challenge gets you in the habit of thinking like an embedded engineer and an ops specialist. Whether you’re hacking tractors or decoding weather sensors, knowing what happened, when, and how is half the job.

---

## 🛠️ Software
- [Visual Studio Code](https://code.visualstudio.com/)
- [Python 3.10+](https://www.python.org/downloads/)
- [PlatformIO Extension for VS Code](https://platformio.org/)
- [Wokwi Extension (for hardware simulation)](https://docs.wokwi.com/vscode/getting-started) [ESP32 Simulator](https://docs.wokwi.com/guides/esp32)
- [Arduino Framework (for C++, via PlatformIO)](https://docs.platformio.org/en/latest/frameworks/arduino.html)
- [ESP-IDF (for C)](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/get-started)

---

## 📋 Recommended Tutorials

Flash MicroPython using the [MicroPython guide](https://randomnerdtutorials.com/getting-started-micropython-esp32-esp8266/).
Send sample data via UART from ESP32 using [Arduino IDE](https://randomnerdtutorials.com/esp32-uart-communication-serial-arduino/) or [PlatformIO](https://randomnerdtutorials.com/vs-code-platformio-ide-esp32-esp8266-arduino/) 
Capture serial in Python with pyserial or via [WebSerial](https://randomnerdtutorials.com/esp32-webserial-library/).
Log terminal commands and serial data
[ESP32 Micropython](https://randomnerdtutorials.com/micropython-esp32-esp8266-vs-code-pymakr/)
[J1939 Preview](https://www.cybertruckchallenge.org/wp-content/uploads/2022/06/Introduction-to-SAE-J1939-CyberTruck-2022.pdf)

