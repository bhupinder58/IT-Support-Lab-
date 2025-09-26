💻 Ticket 07 - Blue Screen on Startup

📝 Issue reported by User: 
_"My laptop reboots with a blue screen every time I log in."_
- **Error observed:** `IRQL_NOT_LESS_OR_EQUAL`
- **Frequency:** Every time the system boots into Windows
- **Last known change:** Installed a third-party VPN client the day before
  
🔍 Troubleshooting Steps

 1. Booted into Safe Mode
- Restarted system and pressed `F8` (or held `Shift` + click **Restart**) to enter **Windows Recovery Environment (WinRE)**
- Navigated to:
  - **Troubleshoot > Advanced Options > Startup Settings**
  - Selected **Enable Safe Mode with Networking**
- System successfully booted into Safe Mode — confirmed issue likely software/driver-related.

---

2. Checked Event Viewer
- Opened **Event Viewer**:  
  `Start > eventvwr.msc`
- Navigated to:  
  `Windows Logs > System`
- Found **critical stop error** entries that pointed to `vpnfilter.sys` (driver for third-party VPN client)
- Event ID: **1001** — BugCheck Code matched blue screen error

---

3. Disabled Startup Items
- Ran `msconfig` to disable all non-Microsoft startup services:
  - Pressed `Win + R`, typed `msconfig`
  - On **Services tab** → Checked "Hide Microsoft services" → Disabled all others
  - On **Startup tab** → Opened Task Manager → Disabled all startup apps

---

4. Uninstalled Problematic Software
- Went to `Control Panel > Programs and Features`
- Found and **uninstalled the VPN software** that introduced the faulty driver
- Rebooted back into normal mode — system booted without blue screen

---

🛠️ Solution (Step-by-Step)

✅ 1. Removed Faulty Driver
- Uninstalled VPN client that installed the faulty kernel driver
- Verified in Device Manager that the driver no longer appeared under Network Adapters or Non-Plug and Play Drivers

---

✅ 2. Repaired System Files

Ran **System File Checker** to ensure no system files were corrupted during crashes:

```powershell
sfc /scannow

Also ran DISM (Deployment Imaging Service Management) to fix deeper system image issues:

DISM /Online /Cleanup-Image /RestoreHealth
```
✅ 3. Updated All Drivers and Windows

- Used Windows Update to install latest patches

- Went to laptop manufacturer’s site and installed:

- Chipset drivers

- Network drivers

- Display drivers

- Ensured all drivers were digitally signed and up to date

✅ 4. (Optional) Reinstalled VPN

- Downloaded the latest version of the VPN software

- Verified it had Windows 10/11 compatibility

- Installed successfully — no blue screen after reboot

✅ Final Status

- System rebooted multiple times without error

- User confirmed normal performance

- VPN working without issues

🔁 Recommendation to User

- Always create a System Restore Point before installing network-related software

- Avoid installing unsigned or outdated drivers from unknown sources

- Schedule automatic driver updates through OEM support software (Dell Update, Lenovo Vantage, etc.)

✅ Status: Resolved
