# 🔐 XYZ Exchange – Securing the Perimeter

**Consultant:** [KSHITIJ PARTE]  
**Roll No:** [CBS-104]

---

## 📜 Project Overview

**XYZ** — a top-tier cryptocurrency exchange — processes over a billion trades daily but fell victim to a devastating network breach due to sloppy perimeter security, costing them over 500 BTC. Ouch. You, as a consultant from SecureCorp, are here to redesign their perimeter network, deploy continuous monitoring, and drive them toward a Zero Trust architecture.

---

## 🛡️ Section 1: Designing a Secure Network Architecture

### ⚡ Current Vulnerabilities
1. **Flat Network Architecture**  
   - All servers sit in one subnet with direct internet access — a dream come true for attackers to pivot internally.

2. **No Firewall Segmentation**  
   - Lack of firewalls leaves internal servers exposed to public traffic with no inspection or control.

3. **Unencrypted Remote Access**  
   - File storage server is accessible directly from the on-premise network over the internet without a secure channel.

---

### 🏗️ Proposed Redesign

- **Network Segmentation:** Separate public-facing (web servers) from internal (databases, storage).
- **Firewalls:** Deploy perimeter firewalls to filter and control incoming/outgoing traffic.
- **VPN:** Secure, encrypted VPN tunnel for on-premise network to reach internal storage safely.

---

### 📣 Stakeholder Justification

**Why firewalls?**  
Firewalls block unauthorized access, control traffic flow, and act as the first line of defense against malicious actors.

**Why network segmentation?**  
Segmentation isolates critical resources — a breach on the web server won’t directly expose the databases.

**Why VPN for storage access?**  
A VPN encrypts data in transit, ensuring only authenticated users can securely access sensitive storage from remote locations.

---

## 💻 Section 2: Building the Architecture in VirtualBox

- **DMZ VNet:**  
  - Subnet 1: Public-DMZ → Web Servers  
  - Subnet 2: Private-DMZ → Database Servers

- **Internal VNet:**  
  - Subnet: Internal-Subnet → File Storage & Internal Services

📸 *Screenshots:*  
- DMZ Virtual Network with subnets  
- Internal Virtual Network with subnet

---

## 🔎 Section 3: Continuous Monitoring with SIEM

### 🎯 SIEM Benefits

1. **Centralized Logging**  
   - Collect logs from all critical points for unified visibility.

2. **Real-time Threat Detection**  
   - Analyze events as they happen, spot suspicious behavior immediately.

3. **Incident Response & Compliance**  
   - Supports rapid detection & investigation while satisfying regulatory requirements.

### 🖥️ VirtualBox Deployment

- Deploy **ELK-Server VM** → Private-DMZ
- Deploy **Filebeat-VM** → Public-DMZ

✔️ *Confirm Screenshots:*  
- ELK server running  
- Filebeat status (`systemctl status filebeat`)  
- Logs visible in Kibana (Hosts/Filebeat-VM)

---

## 🔐 Section 4: Zero Trust

### ⚔️ Principles Compared

| Principle | Zero Trust | Traditional Model | Benefit |
|-----------|-------------|-------------------|---------|
| **Per-session Access** | Access granted per session, minimal duration | Static, long-lived access | Limits window of exploitation |
| **Continuous Monitoring** | Ongoing checks of asset integrity & security | Periodic reviews only | Detect threats faster |
| **Dynamic Authentication** | Context-based, continuous re-auth | One-time login, persistent trust | Prevents stolen creds from working |

---

### 🧩 Recommended Zero Trust Model

✅ Selected Model: "Enclave Gateway" 

Why? 

An Enclave Gateway segments sensitive assets into secure enclaves, enforcing strict access controls and continuous validation. Perfect for XYZ’s diverse infrastructure needing isolated trust zones — while fixing their biggest perimeter flaw: unrestricted internal access.



MIT — Steal this idea, but not XYZ’s crypto.

Delivered by [KSHITIJ PARTE ], making networks too spicy for hackers to swallow.
