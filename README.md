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

BLOCK USER ACCESS TO THE MALICOUS URL (FIREWALL, DNS FILTERING, ECT)



ADD THE SIGNATURE FOR THE ATTACHMENT TO YOUR ANTIVIRUS



CHECK THE IMPACT OF THE EMAIL
- named recipients
- forwarding rules
- delegate access
- distribution groups



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

Interview users
- Did you open the email?
- Did you click a link/Open an attachment?

Identity
- Lock out all user sessions
- Change user passwords
- Change password for apps
- Check login activity across windows, apps, and files
   Time stamps, devices, app IDs, user-agent string

Network
- Check incoming/outgoing connections
- List App IDs to which the users have access

Computer/Devices
- List computers and devices under the user's control 
- Quarantine the devices with suspicious logins
- Check created processes
- Virus scan
- Device forensics

Applications
- Apps to which the users have access
- Time stamps, user-agent string

























