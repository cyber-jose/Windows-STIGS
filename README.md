# 🛡️ Windows STIG Compliance Scripts

Below you'll find a collection of PowerShell scripts created to automate the remediation of Windows 10 security findings based on **DoD Security Technical Implementation Guides (STIGs)**. Each script targets a specific STIG finding and configures system settings to ensure compliance.

---

## 📜 About

This repository provides STIG compliance automation using PowerShell for Windows 10 environments. These scripts modify local security policies and registry settings to enforce Department of Defense (DoD) hardening standards.

Each script includes:
- STIG ID (e.g., `WN10-CC-000020`)
- Description of the control
- Registry or policy changes applied
- Usage instructions
- Testing details

---

## 🧰 Requirements

- Windows 10 Pro or Enterprise (tested on 22H2)
- PowerShell 5.1+
- Administrator privileges

---

## ✅ STIG Remediation Overview

### WN10-AC-000010 – Limit Failed Login Attempts

To mitigate brute-force attacks, this control limits failed login attempts before a lockout occurs. The script configures the `MaxBadPasswordsBeforeLock` registry value to 3.

📄 [View Script](https://github.com/cyber-jose/Windows-STIGS/blob/main/WN10-AC-000010)

---

### WN10-CC-000020 – Disable IPv6 Source Routing

This STIG requires disabling IPv6 source routing to prevent potential misuse by attackers for traffic redirection or reconnaissance. The script sets the `DisableIPSourceRouting` registry key to `2`, which fully disables this behavior.

📄 [View Script](https://github.com/cyber-jose/Windows-STIGS/blob/main/WN10-CC-000020)

---

### WN10-CC-000065 – Disable Wi-Fi Sense

Wi-Fi Sense, a Windows feature designed to simplify wireless connectivity, can unintentionally expose networks. This script disables all related registry settings to ensure no automatic or shared network connections occur.

📄 [View Script](https://github.com/cyber-jose/Windows-STIGS/blob/main/WN10-CC-000065)

---

### WN10-CC-000260 – Enforce Minimum PIN Length

To strengthen authentication, this STIG mandates a minimum PIN length for Windows Hello. The script enforces a minimum of six characters by updating the appropriate registry key.

📄 [View Script](https://github.com/cyber-jose/Windows-STIGS/blob/main/WN10-CC-000260)

---

### WN10-CC-000150 – Require Password on Wake (AC Power)

Systems must prompt for a password when resuming from sleep while connected to AC power. This script sets the necessary Group Policy registry key to enforce that behavior.

📄 [View Script](https://github.com/cyber-jose/Windows-STIGS/blob/main/WN10-CC-000150)

---

### WN10-CC-000160 – Require Password on Wake (DC Power)

This STIG ensures password protection is enforced when waking from sleep on battery power (DC). The script modifies power scheme settings across all active configurations using `powercfg`.

📄 [View Script](https://github.com/cyber-jose/Windows-STIGS/blob/main/WN10-CC-000160)

---

### WN10-CC-000145 – Require Password on Wake (Battery)

This setting enforces that users must re-authenticate when a system resumes from sleep while on battery. The script updates the `RequirePasswordOnWake` registry value accordingly.

📄 [View Script](https://github.com/cyber-jose/Windows-STIGS/blob/main/WN10-CC-000145)

---

## 🚀 Usage

Run scripts individually based on the STIG finding you're remediating.

Example .\WN10-CC-000150.ps1

# Disclaimer

These scripts are provided as-is with no warranty. Always test in a lab environment before deploying to production systems.



