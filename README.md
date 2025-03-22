# **Smart Home System**

## **Project Overview**
This Smart Home system is designed to provide remote and local control over household appliances, enhancing convenience and security. It allows users to control lamps, a door, and an air conditioning unit through a mobile app, PC, or an LCD-keypad interface. The system features an admin-user login, security mechanisms, and EEPROM storage to retain data after power loss.

---

## **Features & Requirements**

### **Control Modes**
- **Remote Control:** Mobile or PC via Bluetooth or TTL module.
- **Local Control:** LCD and keypad (for user mode only).

### **Controllable Devices**
- **Lamps:** 5 on/off lamps and 1 dimmable lamp.
- **Door:** Servo motor-controlled (admin-only access).
- **Air Conditioner:** Controlled by ambient temperature (DC motor).

### **Security & Access Control**
- **Login System:**
  - Admin (remote only)
  - User (local and remote)
- **Admin Privileges:**
  - Can register/remove users.
  - Has full control over all devices.
  - Can lock user access.
- **User Privileges:**
  - Can control all devices except the door.
- **Security Measures:**
  - Usernames and passwords stored in EEPROM.
  - Three failed login attempts trigger system lock and fire alarm until reset.

### **LCD & Keypad Functionality**
- Displays running devices.
- Allows local control when the remote system is unavailable.

### **Bluetooth & TTL Communication**
- Transmits and receives commands between the microcontroller and PC/mobile.
- Displays system messages on PC/mobile.

### **Device Specifications**
#### **Lamps, Relay, and Dimmer**
- Isolated circuits for safety.
- Dimmer controls lamp brightness via 0-5V input.

#### **Temperature Sensor & Air Conditioning**
- Runs the air conditioner if the temperature exceeds **28°C**.
- Turns off the air conditioner if the temperature drops below **21°C**.

#### **Door Control (Servo Motor)**
- Admin-only access to open/close the door via remote commands.

---

## **Hardware Components**
1. **Microcontroller** (Arduino or equivalent)
2. **Memory:** 24C08 EEPROM (or internal EEPROM)
3. **Communication Modules:** HC-05 Bluetooth or TTL (PL2003/CH340/CP2102)
4. **Relays & Transistors:** 5 transistors & relays (or LEDs for simulation)
5. **Dimmer Circuit:** 1 transistor + solid-state relay
6. **Temperature Sensor:** LM35 or equivalent
7. **Motor Drivers:** 2 NPN transistors + DC motor (for air conditioning)
8. **User Interface:** Keypad & LM01602A Character LCD
9. **Servo Motor** (for door control)

---

## **Implementation Options**
- **Hardware-based** (Physical components setup).
- **Simulation-based** (Using software like Proteus, Tinkercad, or Multisim).

---


## **How to Run the Project**

### **Hardware Setup**
1. Connect all components according to the circuit diagram.
2. Upload the microcontroller code via Arduino IDE.
3. Power up the system and test functionalities.

### **Software Setup**
1. Install necessary drivers for Bluetooth/TTL communication.
2. Use a terminal or mobile app to send commands remotely.
3. Monitor responses on LCD and mobile/PC screen.

---

## **Future Enhancements**
- Integration with Wi-Fi for online control.
- Adding voice command support.
- Implementing a mobile app with a graphical interface.

