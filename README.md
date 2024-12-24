# Wireless One-Way Audio Communication System

## Overview
This project demonstrates a **wireless one-way audio communication system** using ESP32 microcontrollers. The system consists of a transmitter and a receiver. The transmitter captures audio through an ISD1820 module and sends it wirelessly using ESP-NOW. The receiver then plays the audio through a speaker powered by an LM386 amplifier module.

---

## Features
- **Wireless Transmission**: Utilizes the ESP-NOW protocol for low-latency communication.
- **Audio Capture and Playback**: The ISD1820 module allows recording and playback of 10-second audio clips.
- **Portable Design**: Powered by rechargeable lithium batteries (2x 18650 per device) with TP4056 charging modules.
- **Long Runtime**: Offers approximately 14 hours of operation on a single charge.
- **Moderate Range**: Covers a distance of up to 50 meters.

---

## System Components

### Transmitter:
1. **ESP32 (ESP32-WROOM)**
2. **ISD1820 voice recorder module**
3. **TP4056 charging module**
4. **Two 3.7V 18650 lithium batteries**
5. Push buttons for ISD1820 module

### Receiver:
1. **ESP32 (ESP32-WROOM)**
2. **LM386 audio amplifier module**
3. **8-ohm 0.5W speaker**
4. **TP4056 charging module**
5. **Two 3.7V 18650 lithium batteries**

---

## Circuit Diagrams
### Transmitter
- Connect the ISD1820 module's PLAY pin to an ESP32 GPIO pin.
- Connect the audio output pin of the ISD1820 to the ESP32 ADC pin.
- Connect the TP4056 output to power the ESP32 and ISD1820.

### Receiver
- Connect the ESP32 DAC pin to the LM386 module's audio input.
- Connect the LM386 output to the speaker.
- Power the ESP32 and LM386 using the TP4056 output.

---

## How to Use
1. **Record Audio (Transmitter):**
   - Press the ISD1820 "REC" button to record a message (max 10 seconds).
   - Press the "PLAY" button to initiate playback and transmission.

2. **Playback Audio (Receiver):**
   - The ESP32 receives audio data via ESP-NOW.
   - The data is processed and sent to the speaker via the LM386 amplifier.

---

## Code
### Transmitter Code
The transmitter code handles:
- Monitoring the ISD1820 "PLAY" signal.
- Capturing audio data.
- Transmitting the data via ESP-NOW.

[**Transmitter Code**]

### Receiver Code
The receiver code handles:
- Receiving audio data via ESP-NOW.
- Playing the audio via the DAC and LM386 amplifier.

[**Receiver Code**] at 

---

## Resources
- [Project Presentation][(link-to-presentation)](https://www.canva.com/design/DAGYbzaA0Gw/dmxJSWVtjwCbh-yXa4wYzQ/view?utm_content=DAGYbzaA0Gw&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=hf7337df1f6)

---

## Contact
Feel free to reach out with any questions or feedback. Let me know if you build something similar!

---

## License
This project is open-source under the MIT License. Contributions are welcome!
