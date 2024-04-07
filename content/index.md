```d2
direction: right

CERT -> Incident Response
Incident Response.shape: text
Incident Response -> Incident Management
Incident Management: |md
    [Incident Management](incident-management.html)
|
Incident Response -> Special Vulnerability Handling
Special Vulnerability Handling.shape: text
CERT -> Cyber Threat Intelligence
Cyber Threat Intelligence: |md
    [Cyber Threat Intelligence](cyber-threat-intelligence.html)
|
#Cyber Threat Intelligence -> Special Vulnerability Handling
CERT -> Digital Forensics
Digital Forensics: |md
    [Digital Forensics](digital-forensics.html)
|
```