# 💻 Precious

**Platform:** Hack The Box  
**OS:** Linux  
**Difficulty:** Easy  
**Category:** Web Application / Privilege Escalation

---

## 📋 Overview

Precious is a Linux machine involving a vulnerable web application that converts web content into PDF documents.

The initial access is obtained by exploiting a vulnerable Ruby PDF generation library. After gaining access to the system, credentials found in a Ruby configuration file allow lateral movement to another user.

Privilege escalation is then achieved by abusing a `sudo` rule that allows the execution of a Ruby script as `root`.

### Attack Path

```text
Web Enumeration
       ↓
PDF Generator
       ↓
Vulnerable Ruby Library
       ↓
Initial Access
       ↓
Credential Discovery
       ↓
User: henry
       ↓
Sudo Enumeration
       ↓
Ruby Script Abuse
       ↓
Root

