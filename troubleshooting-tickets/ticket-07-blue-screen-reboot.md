💻 Ticket 07 - Blue Screen on Startup

📝 Issue reported by User: 
_"My laptop reboots with a blue screen every time I log in."_

🔍 Troubleshooting Steps

1. Booted into Safe Mode – successful  
2. Reviewed `Event Viewer` – Critical error from faulty driver  
3. Last installed item: third-party VPN client  
4. Used `msconfig` to disable startup items  
5. Uninstalled VPN software in Safe Mode

🛠️ Solution

- Removed faulty VPN driver in Safe Mode
- Ran `sfc /scannow` to repair system files
- Rebooted – system stable
- Installed latest version of VPN client (if needed)

✅ Status: Resolved
