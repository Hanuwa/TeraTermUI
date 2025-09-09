# 🔒 How We Protect Your Student Number and PIN


The `SecureDataStore` system protects sensitive credentials, such as student numbers and PINs, when you **choose to save them locally** on a Windows device. Saving is completely optional , you can always enter your details manually instead. 
When used, the system applies AES-GCM-256 encryption for confidentiality and integrity, while the encryption keys themselves are protected through a layered approach: a random master key is bound to your user and device using Windows DPAPI, 
and each key also has a unique passphrase stored securely in Windows Credential Manager. To prevent tampering, the key file (`masterkey.json`) is signed with HMAC-SHA256, and its access is restricted so only the current Windows user can read it. 
The system also handles automatic key rotation, atomic file updates, and secure retirement of old keys. Together, these measures ensure that even if the key file is copied or exposed, it cannot be decrypted or modified without access to both your Windows account and Credential Manager.

## ✅ What We Do
- **AES-GCM-256 encryption** – strong encryption with integrity checks.  
- **Key derivation with HKDF-SHA256**, using:  
  - A **random master key** protected by **Windows DPAPI** (tied to your user + device).  
  - A **per-key random passphrase** stored in **Windows Credential Manager**.  
- **Tamper detection** – `masterkey.json` is signed with **HMAC-SHA256**.  
- **File protection** – restricted to your Windows user (**ACL**) and hidden.  
- **Safe updates** – written atomically (temp file → fsync → secure replace).  
- **Key auto-rotation** – every 90 days by default; old keys are kept temporarily for decryption, then retired.  

---

## 📂 What We Store
- Your **student number and PIN (encrypted only)** – never plaintext on disk.  
- `masterkey.json` – contains encrypted keys, safe metadata, and HMAC.  
- **Per-key passphrases** – stored in **Windows Credential Manager** (scoped to your account).  

---

## 🛡️ What This Protects Against
- Theft or tampering of the key file alone.  
- Casual access by other users on the same machine.  
- Data loss from partial/corrupt writes during updates.  

---

## ⚠️ Limitations (Important)
Even with protections, risks remain:  
- If **malware runs as you**, it can:  
  - Access DPAPI and Credential Manager.  
  - Read secrets from app memory during use.  
  - Keylog your PIN when you type it.  
- **Admins/system-level attackers** can bypass local protections.  
- **Moving files to another device** won’t work (DPAPI-bound).  
- **Losing your Windows profile or Credential Manager items** = unrecoverable data.  

---

## 💡 Tips for Extra Security
- Keep **Windows updated** and run **reputable anti-malware**.  
- Turn on **BitLocker or full-disk encryption**.  
- **Lock your session** when away.  
- Avoid **copying credentials to the clipboard**.  
