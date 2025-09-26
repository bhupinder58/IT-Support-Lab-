
🖨️ Ticket 01 - Printer Not Working


📋 Issue reported by User:
"I can't print anything. The printer shows up on my computer, but nothing comes out."

- **Printer Model:** HP LaserJet Pro M404dn (network printer)
- **Connection Type:** Wired Ethernet
- **Operating System:** Windows 10 Pro x64
- **User Role:** Standard domain user

---

🔍 Troubleshooting Steps (In Detail)

### 1. Verified Physical Connections
- Checked printer's power cable and network cable — ✅ All plugged in securely
- Printer display showed **Ready**, no error messages

---

2. Checked Printer Status in Windows
- Opened **Control Panel > Devices and Printers**
- Printer was listed as **Default**, but had a **status of "Offline"**

---

3. Pinged the Printer
- Got printer’s IP from printer display menu (e.g., `192.168.1.55`)
- Opened Command Prompt:
  ```bash
  ping 192.168.1.55
  ```
- Response: **Request timed out**
- Indicated printer not reachable over the network

---

4. Restarted the Printer
- Power-cycled the printer
- Waited for it to come online
- Pinged again — ✅ Success

---

5. Removed and Reinstalled Printer
- Went to **Settings > Devices > Printers & Scanners**
- Removed the printer
- Clicked **Add a printer** → Chose **The printer that I want isn't listed**
- Entered IP manually: `http://192.168.1.55`
- Driver installed automatically

---

6. Checked Print Spooler Service
- Pressed `Win + R`, typed `services.msc`
- Located **Print Spooler** service:
  - Status: Running
  - Restarted the service to clear any stuck print jobs

---

7. Printed Test Page
- Right-clicked printer → **Printer Properties** → Printed a **Test Page**
- ✅ Test page printed successfully

---

🛠️ Solution Summary

1. Power-cycled printer to restore network connectivity
2. Reinstalled printer using IP address
3. Restarted Print Spooler service
4. Verified successful communication with test page

---

✅ Final Status

- Printer is online and functional
- User able to print without issue
- No hardware fault found — resolved through network and software reset

---

🧠 Recommendations

- Assign printer a **static IP** via DHCP reservation to avoid future IP conflicts
- Educate user on how to check printer status from **Devices and Printers**
- Set up basic logging on print server (if applicable)

---

 ✅ Status: Resolved

