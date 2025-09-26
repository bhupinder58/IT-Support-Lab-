🔌 Ticket 05 - USB Device Not Recognized

📝 Issue reporeted by User:
"My USB flash drive isn’t working on my laptop. It says: 'USB device not recognized'."

🔍 Troubleshooting Steps


1. Plugged USB into a second port — same issue.
2. Tried the USB on another laptop — worked fine.
3. Opened **Device Manager** → Yellow exclamation under `Universal Serial Bus controllers`
4. Right-clicked → Properties → Status: “Unknown device”
5. Verified Windows is fully updated.

---

🛠️ Solution (Detailed)

1. **Uninstall and Reinstall USB Drivers:**
   - Device Manager → Right-click "Unknown Device" → Uninstall
   - Rebooted PC → Windows reinstalled drivers

2. **Reset USB Controllers:**
   - In Device Manager → Uninstalled all under "Universal Serial Bus Controllers"
   - Rebooted system

3. **Power Cycle the System:**
   - Shut down completely
   - Unplugged power for 1 minute
   - Booted up → Plugged in USB again → Detected

4. **Disable USB Selective Suspend:**
   - Control Panel → Power Options → Advanced Settings
   - USB settings → Set **USB selective suspend setting** to Disabled

5. **Check BIOS/UEFI:**
   - Ensured USB ports weren’t disabled in BIOS

---

✅ Status: Resolved (USB device detected after reboot and driver reinstall)
