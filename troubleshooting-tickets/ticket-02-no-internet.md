🌐 Ticket 02 - No Internet Access


📋 Issue reported by User: 

"I’m connected to Wi-Fi, but I can't access any websites. It says 'No Internet Access' at the bottom."

- **Device Type:** Laptop (Windows 10 Pro x64)
- **Connection Type:** Wireless
- **Other Devices on Network:** Working fine
- **Reported Time:** Morning after returning from weekend

---

🔍 Troubleshooting Steps (In Detail)

1. Verified Wi-Fi Connection
- Confirmed user is connected to correct SSID: `Office-WiFi`
- Network icon shows yellow triangle – "Connected, No Internet"
- Checked other devices on the same Wi-Fi – ✅ All working

---

2. Ran IP Configuration Check
- Opened **Command Prompt**, ran:
  ```bash
  ipconfig /all
  ```
- Found:
  - IP Address: `169.254.x.x` → **APIPA address**
  - No default gateway assigned
  - Indicates DHCP server not reachable

---

3. Released and Renewed IP Address
```bash
ipconfig /release
ipconfig /renew
```
- Still received APIPA address
- Confirmed issue with DHCP communication on this machine

---

4. Flushed DNS and Reset Winsock
Ran the following network reset commands:
```bash
ipconfig /flushdns
netsh winsock reset
netsh int ip reset
```
- Rebooted machine after commands
- Still no valid IP received

---

5. Checked Wireless Adapter Driver
- Opened **Device Manager > Network Adapters**
- Right-clicked Wi-Fi adapter → Properties
- Driver status: "This device is working properly"
- Updated driver just in case → Used **Search automatically** option
- ✅ Driver updated and reinstalled

---

6. Tested Static IP Configuration
- Manually assigned:
  - IP: `192.168.1.99`
  - Subnet Mask: `255.255.255.0`
  - Gateway: `192.168.1.1`
  - DNS: `8.8.8.8`
- Able to **ping router** and **Google DNS**
  ```bash
  ping 8.8.8.8
  ```
- Internet started working — confirmed **DHCP issue**

---

7. Checked Windows Services
- Ran `services.msc` and ensured the following were **running**:
  - **DHCP Client**
  - **DNS Client**
  - **Network Location Awareness**
- Restarted **DHCP Client** service — received IP after restart

---

🛠️ Final Solution (Step-by-Step)

1. Rebooted laptop and reset network settings
2. Verified Wi-Fi adapter driver and updated it
3. Restarted DHCP Client service
4. System received a valid IP from DHCP server
5. Restored automatic IP settings after static IP test

---

✅ Final Status

- Device successfully reconnected to Wi-Fi with valid IP
- Internet access restored
- Verified by browsing multiple websites and running speed test
- No hardware issue detected

---

🧠 Recommendations

- Regularly update Wi-Fi drivers from OEM site
- Avoid powering off router abruptly over weekends
- Use static IP only for troubleshooting — not permanent setup

---
✅ Status: Resolved
