🐢 Ticket 03 - Slow PC Performance

📝 Issue Reported by User:
"My PC has been running extremely slow since last week. Programs take forever to open."


🔍 Troubleshooting Steps

1. Opened **Task Manager** to analyze resource usage.
   - Observed high CPU usage (90–100%) and high disk usage from background tasks.
2. Identified that `Windows Search` and `OneDrive` sync were consuming resources.
3. PC has only 4GB RAM and a mechanical hard drive (HDD).
4. Scanned for malware using **Windows Defender** — no threats found.
5. Checked **Startup tab** in Task Manager — many unnecessary apps auto-loading at boot.


🛠️ Solution

1. **Disable Startup Programs:**
   - Open Task Manager → Startup tab
   - Disabled non-essential apps like:
     - Spotify
     - Zoom
     - Microsoft Teams (if not used regularly)

2. **Turn Off Search Indexing:**
   - Press `Win + R` → Type `services.msc`
   - Find **Windows Search** → Right-click → Properties → Set Startup type to `Disabled`

3. **Pause OneDrive Sync (Optional):**
   - Right-click OneDrive in taskbar → Pause syncing for 24 hours

4. **Disk Cleanup and Optimization:**
   - Run `cleanmgr` → Select C: → Remove temporary files
   - Run **Defragment and Optimize Drives** → Optimize C: drive

5. **Performance Power Plan:**
   - Go to Control Panel → Power Options → Set to **High Performance**

6. **Recommendations to User:**
   - Upgrade RAM to **8GB minimum**
   - Replace HDD with **SSD** for major performance boost

---

✅ Status: Resolved (Performance noticeably improved after cleanup; upgrade planned)
