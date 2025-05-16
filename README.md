# Project-1-Analysing-Phishing-Emails
Analyse the Body of the Email

For this project, I´ve used the following website to get free phishing emails to analyse: phishing_pot/email at main · rf-peixoto/phishing_pot · GitHub and I´ve selected an email 

Original url: https://heritagejewelryandloan.com 
About Heritage Jewelry and Loan is a pawn shop located in Sugar Land, Texas. The business offers 10% interest pawn loans and is known for its fair, compassionate, and transparent dealings. Opened in 2005

Tool used to verify email: https://mxtoolbox.com/EmailHeaders.aspx 

GOAL: Review the email to confirm if it is a Pishing email or not.

Step 1: Identify any red flags for each bullet point in the body of the email:


1) Unfamiliar sender or email address: The email is from someone you don't recognise, or the domain is slightly misspelt (e.g., "support@paypa1.com" instead of "support@paypal.com").
2) Urgent or alarming language: The email pressures you to act immediately, often threatening consequences if you don’t.
3) Suspicious attachments or links: Unexpected attachments or links that request sensitive information or lead to unfamiliar websites.
4) Generic greetings: Using broad salutations like "Dear Customer" instead of addressing you by name.
5) Spelling and grammar mistakes: Phishing emails often contain poor grammar, awkward language, or spelling errors.
6) Request for personal or financial information: Asking for passwords, credit card numbers, or other sensitive information.
7) Mismatch between display name and email address: The name shown in the email may not match the actual email address.
8) Inconsistent or suspicious URLs: Hover over links without clicking to check if the destination URL matches the claimed website.
9) Unexpected request for payment: An email asking for payment for a service you don't recognise or weren't expecting.
10) Too good to be true offers: Promises of large rewards, cash prizes, or free gifts that seem unrealistic.
11) Unfamiliar or odd attachments: Unexpected file attachments, especially if they have unusual extensions like .exe, .zip, or .rar.
12) Lack of company branding: Legitimate companies typically include professional logos, branding, and consistent formatting.
13) Unusual sender’s email domain: The email might come from a suspicious or untrusted domain, rather than an official company email (e.g., "info@gmail.com" instead of "support@company.com").
14) No signature or contact information: Legitimate companies usually include proper signatures and contact details at the end of their emails.

Step 2: Analyse the Body of the Email:

1) "From" Address:
Check the sender's email address for inconsistencies or slight misspellings that mimic legitimate domains (e.g., "support@paypa1.com" instead of "support@paypal.com").
Verify if the domain matches the supposed sender's official domain.
In this example From address: "Mary" <noreply@att.net>

2) "Reply-To" Address
Inspect the "Reply-To" field. Phishing emails often use a different reply address than the "From" address, redirecting replies to the scammer.

In this example Reply-To Address is the same: noreply@att.net

3) "Received" Fields
Check the "Received" headers to trace the path of the email. Compare the IP addresses and domains to ensure they originate from a legitimate source.
If the email claims to be from a well-known service but the IP belongs to an unrelated provider, this is suspicious.
In this example, domain from: her.heritagejewelryandloan.com (192.232.233.127) Real domain:  https://heritagejewelryandloan.com 

4) IP Address and Domain Reputation
Analyse the IP addresses in the "Received" fields. Use tools like MXToolbox or IPVoid to check if the IP is associated with phishing or spam.
Look up the sending domain for any blacklists or warnings using domain reputation tools like Whois or MXToolbox.



5) External Links and Attachments
Hover over any links to inspect their true destination. Ensure they match the expected domain (e.g., "delivero[.]com"). Use tools like VirusTotal or PhishTank to scan URLs for malware or phishing attempts.
Do not download or open any attachments unless you are certain of their legitimacy. Suspicious attachments should be scanned using antivirus software or online services like VirusTotal to check for malware.

5) DKIM Signature (DomainKeys Identified Mail)
DKIM verifies if the email was sent by the legitimate domain. Check if the DKIM signature in the header is valid and aligned with the domain of the email sender.
Using MXToolBox, DKIM Alignment is wrong:

I´ve included the first part of the real and fake information:




6) SPF Record (Sender Policy Framework)
Look for an SPF record result in the header, indicating if the email passed or failed SPF authentication. A pass means the email came from an authorised server for that domain.
If it fails, it's a sign the email may be forged.

7) DMARC Authentication
DMARC (Domain-based Message Authentication, Reporting & Conformance) ensures the email’s authenticity. Look for pass or fail results, which indicate whether the message aligns with SPF and DKIM policies.



8) Message-ID
Every legitimate email has a unique Message-ID. Check for strange patterns in this field, such as missing, repeated, or generic message IDs, which can indicate spoofing.


9) Subject Encoding and Language
Review the subject line for suspicious characters, encoding issues, or misspellings. Malicious actors often use strange encoding or poorly constructed subjects to bypass filters.


10) MIME-Version
Check the MIME-Version field to see how the email’s format is structured. Irregular MIME types or missing headers may indicate an attempt to manipulate the format for malicious purposes.


CONCLUSION:
Phishing likelihood: High. The misspelt domain ("delivero[.]com"), failed DMARC check, and redirection to a suspicious domain are significant indicators of phishing. Additionally, the "From" and "Reply-To" addresses were different from the "Received" section, further raising suspicion that the email may have been spoofed or manipulated.


