# Windows Read-Only Security Audit

PowerShell script for **read-only** security auditing of Windows servers, focused on security posture, compliance, and operational visibility.

Designed to run safely in **production environments** without changing system configuration.

---

## 🎯 Purpose

Provide a reliable technical snapshot of Windows server security and configuration for:
- Internal audits
- Compliance assessments
- Security baselines
- Due diligence
- Technical inventory

---

## 🛡️ Security principles

- **READ-ONLY (SAFE MODE)** execution
- No changes to:
  - Registry
  - Services
  - Policies
  - System configuration
- No `Invoke-Expression`
- Robust error and timeout handling
- Evidence preserved with metadata

---

## 🔍 Audit scope

- Operating system information
- Last boot time
- Installed patches / hotfixes
- Windows Update configuration
- Microsoft Defender status
- Firewall (Domain / Private / Public)
- SMB (including SMBv1)
- RDP and NLA
- TLS / Schannel
- Audit policies (`auditpol`)
- Local accounts
- SHA256 hashes of generated artifacts

---

## ▶️ Execution

```powershell
powershell.exe -NoProfile -ExecutionPolicy Bypass `-File "Invoke-WindowsServerReadOnlyAudit.ps1"
```
