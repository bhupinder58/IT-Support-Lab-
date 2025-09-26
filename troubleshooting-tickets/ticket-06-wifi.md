📡 Ticket 06 - Wi-Fi Keeps Dropping

📝 Issue reported by User:
_"Wi-Fi disconnects every 5–10 minutes, especially during video calls."_

🔍 Troubleshooting Steps

1. Confirmed user was close to router (good signal strength)
2. Noted disconnections happen more on battery mode
3. Checked Event Viewer → Network Adapter Power Management logs
4. Device Manager → Wireless adapter was using outdated driver
5. Noticed connection to 2.4GHz band (slower and interference-prone)

---

🛠️ Solution (Detailed)

1. **Update Wireless Adapter Driver:**
   - Device Manager → Network Adapters → Right-click Wi-Fi → Update driver
   - Used manufacturer’s website (Intel/Realtek) for latest version

2. **Disable Power Saving on Wi-Fi Adapter:**
   - Device Manager → Wi-Fi adapter → Properties → Power Management
   - Unchecked **“Allow the computer to turn off this device to save power”**

3. **Switch to 5GHz Band:**
   - Logged into router (e.g., 192.168.1.1)
   - Separated SSIDs for 2.4GHz and 5GHz
   - Connected user to 5GHz (faster and more stable)

4. **Flush and Reset Network Settings:**
   ```powershell
   ipconfig /release
   ipconfig /renew
   ipconfig /flushdns
   netsh winsock reset
   netsh int ip reset
5. Update Router Firmware (if user has access):

   Checked for outdated firmware and applied update.

✅ Status: Resolved (Stable Wi-Fi for 3 days; no further drops)

---







   
