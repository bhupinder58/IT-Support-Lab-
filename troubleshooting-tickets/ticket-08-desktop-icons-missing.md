🖥️ Ticket 08 - Desktop Icons Missing

📝 Issue Reported by User:  
"All of my desktop icons are missing. My wallpaper is still there, but none of my files or shortcuts are showing up."

- **System:** Windows 10 Pro (x64)
- **User account:** Local standard user
- **Last known change:** None reported; started happening after a Windows update

  
🔍 Troubleshooting Steps

1. Checked Desktop View Settings
- Right-clicked on Desktop → Hovered over **View**
- **“Show Desktop Icons” was unchecked**
- Re-enabled the setting by clicking it → Icons immediately reappeared

✅ Quick fix, but continued to investigate to ensure no deeper problem.

---

2. Checked Desktop Files Directory
- Opened File Explorer → Navigated to:
  ```
  C:\Users\<username>\Desktop
  ```
- All files and shortcuts were present and intact
- Confirmed data was not lost — just hidden from the desktop UI

---

3. Verified `explorer.exe` Was Running
- Pressed `Ctrl + Shift + Esc` to open **Task Manager**
- Confirmed that `explorer.exe` was running
- As a precaution:
  - Right-clicked `explorer.exe` → **End task**
  - Clicked **File > Run new task** → Entered `explorer.exe` → Clicked OK
- Desktop refreshed correctly

---

4. Checked for Tablet Mode (Windows 10)
- Opened **Action Center** (Win + A)
- Found **Tablet Mode** was enabled (can hide desktop icons)
- Toggled **Tablet Mode OFF**
- Desktop icons reappeared after switch

---

5. Checked Group Policy (For Managed Systems)
> *Not applicable for this user, but important in enterprise environments:*

- Ran `gpedit.msc`
- Navigated to:  
  `User Configuration > Administrative Templates > Desktop`
- Ensured policy **"Hide and disable all items on the desktop"** was set to **Not Configured**

---

🛠️ Solution (Step-by-Step Summary)

1. **Re-enabled Desktop Icons:**
   - Right-clicked on Desktop → View → ✅ Checked **"Show Desktop Icons"**

2. **Disabled Tablet Mode:**
   - Opened Action Center → Turned **Tablet Mode OFF**

3. **Restarted Windows Explorer (Optional):**
   ```powershell
   taskkill /f /im explorer.exe
   start explorer.exe
   ```

4. **User Education:**
   - Showed the user how to toggle icon visibility in case it happens again
   - Explained how Tablet Mode changes interface behavior

---

✅ Final Status

- Desktop icons successfully restored
- No data loss occurred
- Issue resolved with user education and interface correction

---

## 🧠 Recommendations

- Avoid accidental changes to display settings
- Create a **System Restore Point** after updates
- Pin important folders like Desktop to **Quick Access** for backup access
- Optionally back up Desktop items to OneDrive or cloud storage

---

✅ Status: Resolved.

This ticket demonstrates:
- Understanding of **Windows Explorer**, display settings, and desktop rendering.
- Ability to identify **non-technical user errors**
- Proper **end-user support and education**
- Awareness of **Windows features** like Tablet Mode and Group Policy.

