****Exploit Title: CMS Made Simple Version: 2.2.21 - Stored XSS**** 

**Date: 2025-05-11**

**Exploit Author: feixuezhi**

**Vendor Homepage: https://www.cmsmadesimple.org/**

**Version: 2.2.21**

**Tested on: https://softaculous.com/demos/cms_made_simple**

**Description:**
CMS Made Simple Version 2.2.21 is vulnerable to Cross Site Scripting (XSS). This vulnerability resides in the Design Manager module of the admin panel. Specifically, the issue arises due to inadequate sanitization of user input in the "Templates Description" field.

**Steps to Reproduce:**
1) Log in as admin and navigate to Layout > Design Manager > Templates.
2) Click on Content -> Content Manager Module
3) Click on "Create a new Template"
4) In "Name" field, input template name
5) Click on "Description"
6) In "Description" field, input payload `</textarea><details open="" ontoggle=alert(document.cookie)><textarea>`
7) Click "Submit"
8) After submitting, payload will be executed every time we click on  "View this page in another window " .

**Notes:**

* This exploit confirms the presence of XSS vulnerability in.
* The payloads are utilized to evaluate expressions and verify the XSS.
* Use responsibly and with proper authorization; unauthorized use of this exploit may lead to legal consequences.
