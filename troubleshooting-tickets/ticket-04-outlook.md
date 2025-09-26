📧 Ticket 04 - Outlook Not Sending Emails

📝 Issue Reported by user:
"Emails are stuck in my Outbox and not sending."

🔍 Troubleshooting Steps

1. Checked internet connection – working.
2. Restarted Outlook – issue persisted.
3. Clicked **Send/Receive All Folders** – no change.
4. Verified account settings under **File > Account Settings > Server Settings** – IMAP and SMTP were correctly configured.
5. Ran **Outlook Repair Tool** – failed.
6. Noticed high mailbox size and corrupted outbox folder.

---

🛠️ Solution 

1. **Clear Outbox Emails:**
   - Switched Outlook to **Offline Mode**
   - Deleted emails stuck in Outbox
   - Switched back to Online

2. **Repair Outlook Profile:**
   - Go to Control Panel → Mail (32-bit) → Email Accounts
   - Selected profile → Clicked **Repair**
   - If still broken, deleted and recreated profile

3. **Reconfigure Email Account:**
   - Re-added account with manual setup
   - Verified:
     - SMTP port = `587` (TLS)
     - IMAP port = `993` (SSL)
     - Authentication = ON

4. **Check Add-Ins:**
   - File → Options → Add-Ins → Disabled any unnecessary or third-party add-ins

---

✅ Status: Resolved (User able to send/receive emails normally)
