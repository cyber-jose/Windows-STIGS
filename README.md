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

## ✅ Remediation Scripts Overview

| STIG ID         | Description                                 | Script Name              |
|-----------------|---------------------------------------------|--------------------------|
| WN10-CC-000020  | Disable IPv6 source routing                 | `WN10-CC-000020.ps1`     |
| WN10-CC-000065  | Disable Wi-Fi Sense                         | `WN10-CC-000065.ps1`     |
| WN10-CC-000260  | Enforce minimum PIN length                  | `WN10-CC-000260.ps1`     |
| WN10-CC-000150  | Require password on wake (AC power)         | `WN10-CC-000150.ps1`     |
| WN10-CC-000160  | Require password on wake (DC power)         | `WN10-CC-000160.ps1`     |
| WN10-AC-000010  | Limit failed login attempts                 | `WN10-AC-000010.ps1`     |
| WN10-CC-000145  | Require password on wake (battery)          | `WN10-CC-000145.ps1`     |

---

## 🚀 Usage

Run scripts individually based on the STIG finding you're remediating.

# Example

.\Fix-WN10-CC-000150.ps1

# Disclaimer

These scripts are provided as-is with no warranty. Always test in a lab environment before deploying to production systems.



