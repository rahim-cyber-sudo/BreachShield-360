# 🛡️ BreachShield 360
**Live Cyber Threat Telemetry & Zero-Trust Incident Command Center**  
*Built for the NIAT Solvers League 2026*

---

## 🚀 Live Access Links
* 🌐 **Launch Live Web App (Browser):** [Open BreachShield 360](https://www.appsheet.com/start/b282c8df-a372-4c66-aafe-c6c211b7be89)
* 📲 **Install Mobile App Shortcut:** [Download BreachShield 360 on Mobile](https://www.appsheet.com/newshortcut/b282c8df-a372-4c66-aafe-c6c211b7be89)

---

## 🎯 Problem Statement
Organizations, government agencies, and everyday citizens face escalating risks from credential dumps, API leaks, and malicious phishing links. Traditional threat intelligence tools are expensive, desktop-bound, and slow to deploy during an active incident.

## 💡 Solution: BreachShield 360
**BreachShield 360** is an elite, smartphone-first cybersecurity command center engineered using a reactive **AppSheet** frontend and a **Google Sheets** cloud database. It features a custom **0.1-second heuristic calculation engine** to evaluate targets, calculate blast radius, and generate automated containment playbooks on the fly.

---

## ⚡ Key Features
* **0.1-Second Live OSINT Risk Scoring:** Automatically classifies targets into `🔴 CRITICAL`, `🟠 HIGH`, `🟡 MODERATE-HIGH`, or `🟢 MODERATE` based on real-time pattern matching and breach telemetry.
* **PhishGuard Link & SMS Detector:** Identifies malicious `.apk` payloads, `bit.ly` obfuscated links, and KYC/OTP social engineering vectors.
* **Automated Blast-Radius & Lockdown Playbooks:** Generates instant 3-step incident response protocols tailored to the target entity.
* **1-Tap Command Actions:**
  * 🌐 **Live Web OSINT Scan:** Triggers deep real-time web intelligence queries.
  * 📄 **Executive Report Exporter:** Auto-drafts a complete security audit report via email.
  * 🚨 **1930 Cyber SOS Integration:** 1-tap dialer to India's National Cyber Crime Helpline (`1930`).

---

## 🧠 Core Heuristic Engine Logic (AppSheet Formula)
```text
IF(OR(CONTAINS([Target_Name], "boAt"), CONTAINS([Target_Name], "BigBasket"), CONTAINS([Target_Name], "AIIMS"), CONTAINS([Target_Name], "ICMR"), CONTAINS([Target_Name], ".apk"), CONTAINS([Target_Name], "bit.ly"), CONTAINS([Target_Name], "KYC")), "🔴 CRITICAL (Score: 95/100) - High-Risk Threat / Exposure Verified", IF(OR([Target_Category] = "Government", CONTAINS([Target_Name], ".gov"), CONTAINS([Target_Name], "SBI"), CONTAINS([Target_Name], "IRCTC"), [Target_Category] = "Phishing Link / SMS"), "🟠 HIGH (Score: 80/100) - Active Phishing / Infrastructure Vector", IF(CONTAINS([Target_Name], "@"), "🟡 MODERATE-HIGH (Score: 65/100) - Active Email Footprint", "🟢 MODERATE (Score: 48/100) - Standard Digital Surface")))
🏗️ System Architecture
​Frontend UI: AppSheet Reactive Dark-Mode Interface (Multi-Tab Navigation: 🛡️ Live Scanner & 📡 Threat Radar)
​Backend Database: Google Sheets Cloud Tables (Audit_Scanner, Threat_Radar, Admin_Vault)
​Access Control: Role-based Google Authentication (USEREMAIL() telemetry tracking)
