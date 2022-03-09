# Phishing-Response-Script
A repository for a script that automates parts of the phisihing response procedure

Sources:
The phishing response playbook in Microsoft Docs
https://docs.microsoft.com/en-us/security/compass/incident-response-playbook-phishing
https://raw.githubusercontent.com/MicrosoftDocs/security/main/compass/media/incident-response-playbook-phishing/PI_flow.png



Actions to Cover (not strictly in order and several things may happen simultaniously)

CHECK THE CONTENT OF THE EMAIL
Sender Email Address
- DMARC
- Check the sender address against known malicious actors

Attachments
- MD5 Hash
- Check against malware

Links
- Check against known malicious websites



If confirmed to be a false positive...
DISCONTINUE RESPONSE



If confirmed to be a phishing email...
BLOCK USER ACCESS WITH THE MALICOUS URL



ADD THE SIGNATURE FOR THE ATTACHMENT TO YOUR ANTIVIRUS



CHECK THE IMPACT OF THE EMAIL
- named recipients
- forwarding rules
- delegate access



GET THE LOGIN ACTIVITY OF CONTACTED USERS
- AD
- AzAD



CHECK USER INTERACTION WITH HE EMAIL
- Clicking links
- Downloading files
- Clicking attachments



For those that didn't interact with the email...
 - Delete the email from their inbox



For those that interacted with the email...
- 




















