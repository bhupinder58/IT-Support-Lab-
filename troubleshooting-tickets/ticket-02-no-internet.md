🌐 Ticket 02 - No Internet Access


📋 Issue

User says:  
"My Wi-Fi is connected, but I can’t access any websites."

🔍 Troubleshooting Steps

1. Confirm network connected ✅  
2. Run `ipconfig /all` → Has IP? ✅  
3. Ping gateway → `ping 192.168.1.1` ✅  
4. Ping DNS → `ping 8.8.8.8` ✅  
5. Ping domain → `ping google.com` ❌

🛠️ Solution

- DNS was not resolving
- Changed DNS to 1.1.1.1 & 8.8.8.8
- Cleared DNS cache: `ipconfig /flushdns`

✅ Status: Resolved

