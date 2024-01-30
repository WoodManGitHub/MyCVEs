# 2024 REDAXO CMS XSS
- **Exploit Title:** REDAXO_CMS_Cross_Site_Scripting
- **Date:** 2024-01-30
- **Exploit Author:** WoodMan
- **Vendor Homepage:** https://redaxo.org/
- **Software Link:** https://github.com/redaxo/redaxo
- **Version:** 5.15.1
- **Tested on:** Kali Linux + Docker
- **Payload:** <script>alert('XSS')</script>
- **CVE:** Reported, waiting for CVE Number

## Description
The 'Name' section in the Template section of the REDAXO CMS is vulnerable to Cross-Site Scripting Attacks. REDAXO is vulnerable to a cross-site scripting vulnerability because it fails to sufficiently sanitize user-supplied data. An attacker may leverage this issue to execute arbitrary script code in the browser of an unsuspecting user in the context of the affected site. This may allow the attacker to steal cookie-based authentication credentials and launch other attacks.

## Proof of Concept
1. Log in as an administrator.
2. Navigate to the Templates page.
3. Create a new template and enter <script>alert('XSS')</script> in the Name field.
4. Return to Structure and create a new Article, selecting the template created in step 3.
5. View the page.
