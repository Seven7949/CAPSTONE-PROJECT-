# Fed F1rst Control Systems – Compliance Assessment 🚀🔒

## 📌 Project Overview

In the fast-paced digital era, **Fed F1rst Control Systems** is pushing the boundaries of cybersecurity. As a security engineer, your mission is to secure Windows and macOS environments, craft ironclad policies, align with **NIST SP 800-53 Rev. 5**, and fortify cloud infrastructure — all to build an unbreakable defense against tomorrow’s cyber threats.

---

## ⚙️ Section 1: Hardening Strategies

### 🪟 Windows 10/11 Hardening
1. **Outdated System Updates**  
   - Enable auto-updates for the latest patches.
2. **Disabled Antivirus**  
   - Activate Windows Defender or install a trusted AV.
3. **Weak Passwords**  
   - Enforce strong, complex password policies.
4. **Firewall Disabled**  
   - Enable Windows Firewall for all profiles.
5. **AutoRun/AutoPlay Enabled**  
   - Disable AutoPlay for all devices.
6. **Inactive Admin Account**  
   - Deactivate default Admin, use a new secured one.

### 🍏 macOS Hardening
1. **FileVault Encryption** – Encrypt the entire drive.
2. **Firewall Activation** – Block unauthorized traffic.
3. **Disable Automatic Login** – Enforce manual authentication.
4. **Enable Gatekeeper** – Allow apps only from verified sources.
5. **Turn Off System Location** – Limit unnecessary location data sharing.
6. **Strong Password & Touch ID** – Use dual authentication.

---

## 📧 Section 2: Security Policies

### ✉️ Email Policy
1. No auto-forwarding to personal emails.
2. Enforce MFA for email logins.
3. Ban opening unknown attachments or suspicious links.
4. Encrypt sensitive emails.
5. Report phishing attempts immediately.

### 📱 BYOD Policy – Security Measures
1. Mandatory full-disk encryption.
2. Screen lock & strong authentication.
3. MDM enrollment required.
4. No rooted/jailbroken devices.
5. Use secure containers for work data.
6. Mandatory incident reporting & remote wipe compliance.

---

## 🗂️ Section 3: Compliance Checks

### ✅ Windows Desktop Compliance (NIST SP 800-53 Rev. 5)
- Built-in Admin disabled
- Firewall enabled
- Auto updates ON
- UAC enabled
- Strong passwords enforced
- Guest account disabled
- System logging/auditing enabled
- Windows Defender active
- Secure Remote Desktop
- IE ESC enabled
- USB restricted
- VLAN & port security
- Remote Registry disabled
- Updates auto-download/install

---

## 🧹 Remediation (Examples)
| Control | Action |
|---------|--------|
| AC-2 | Disable unused accounts; set expiration |
| AC-6 | Remove admin rights; apply RBAC |
| AU-2 | Enable event logging via GPO |
| AU-6 | Schedule log reviews |
| IA-2 | Enforce password complexity |
| IA-5 | Force password expiration/reuse prevention |
| SC-7 | Enable firewall; restrict inbound ports |

---

## 🐧 Linux Compliance (CMMC)
- Current updates applied
- `/var` partition separate
- Automounting disabled
- AIDE installed
- Unnecessary services (daytime, echo, tftp, CUPS, DHCP, FTP, Samba) disabled
- TCP Wrappers & iptables installed
- DCCP disabled
- Audit log size set; auto-deletion disabled

---

## ☁️ Section 4: Cloud Security

### 🖥️ Windows Server Build Sheet
- Latest OS version (e.g., Server 2022)
- Only needed server roles installed
- Proper firewall rules (default deny)
- Hardened admin accounts
- Automatic updates configured
- Antivirus/threat protection enabled
- Logging & monitoring integrated with SIEM
- Encrypted backups & recovery tested
- SSL/TLS properly configured
- Secure RDP with NLA/MFA

### ☁️ CASB Benefits
1. Visibility into cloud storage & shadow IT.
2. Data Loss Prevention for sensitive files.
3. Advanced threat protection.
4. Simplified compliance (GDPR, HIPAA, PCI).
5. Conditional access controls for users/devices.

---

## 👤 Author

KSHITIJ PARTE  
_CBS-0104_

---

## 🔗 License

MIT — reuse, remix, fortify 🔐


