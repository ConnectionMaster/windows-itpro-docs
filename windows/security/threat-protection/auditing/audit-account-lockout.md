---
title: Audit Account Lockout (Windows 10)
description: This topic for the IT professional describes the advanced security audit policy setting, Audit Account Lockout, which enables you to audit security events that are generated by a failed attempt to log on to an account that is locked out.
ms.assetid: da68624b-a174-482c-9bc5-ddddab38e589
ms.pagetype: security
ms.prod: w10
ms.mktglfcycl: deploy
ms.sitesec: library
author: Mir0sh
ms.date: 04/19/2017
---

# Audit Account Lockout

**Applies to**
-   Windows 10
-   Windows Server 2016


Audit Account Lockout enables you to audit security events that are generated by a failed attempt to log on to an account that is locked out.

If you configure this policy setting, an audit event is generated when an account cannot log on to a computer because the account is locked out. Success audits record successful attempts and failure audits record unsuccessful attempts.

Account lockout events are essential for understanding user activity and detecting potential attacks.

**Event volume**: Low.

This subcategory failure logon attempts, when account was already locked out.

| Computer Type     | General Success | General Failure | Stronger Success | Stronger Failure | Comments                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------|-----------------|-----------------|------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Domain Controller | No              | Yes             | No               | Yes              | We recommend tracking account lockouts, especially for high value domain or local accounts (database administrators, built-in local administrator account, domain administrators, service accounts, domain controller accounts, and so on).<br>This subcategory doesn’t have Success events, so there is no recommendation to enable Success auditing for this subcategory. |
| Member Server     | No              | Yes             | No               | Yes              | We recommend tracking account lockouts, especially for high value domain or local accounts (database administrators, built-in local administrator account, domain administrators, service accounts, domain controller accounts, and so on).<br>This subcategory doesn’t have Success events, so there is no recommendation to enable Success auditing for this subcategory. |
| Workstation       | No              | Yes             | No               | Yes              | We recommend tracking account lockouts, especially for high value domain or local accounts (database administrators, built-in local administrator account, domain administrators, service accounts, domain controller accounts, and so on).<br>This subcategory doesn’t have Success events, so there is no recommendation to enable Success auditing for this subcategory. |

**Events List:**

-   [4625](event-4625.md)(F): An account failed to log on.
