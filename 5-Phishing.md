 Phishing are common social engineering attacks. In social engineering, phishing attack vectors can be a phone call, a text message, or an email.

  first email classified as spam dates back to 1978


   The person responsible for the contribution to the way we communicate was <font color=red>Ray Tomlinson.</font>

Parts of email
- User Mailbox (or Username)
- @
- Domain



- SMTP (Simple Mail Transfer Protocol) - It is utilized to handle the sending of emails. 
- POP3 (Post Office Protocol) - Is responsible transferring email between a client and a mail server. 
- IMAP (Internet Message Access Protocol) - Is responsible transferring email between a client and a mail server. 



POP3 - on device | IMAP - server config







- Urgency
- HTML to impersonate a legitimate brand
- Link manipulation
- Credential harvesting
- Poor grammar and/or typos




## List of artefacts to be collected

Below is a checklist of the pertinent information an analyst (you) is to collect from the email header:

- Sender email address
- Sender IP address
- Reverse lookup of the sender IP address
- Email subject line
- Recipient email address (this information might be in - - the CC/BCC field)
- Reply-to email address (if any)
- Date/time
- Any URL links (if an URL shortener service was used, then we'll need to obtain the real URL link)
- The name of the attachment
- The hash value of the attachment (hash type MD5 or - - - SHA256, preferably the latter)
- defang url


## Email Header analys
https://toolbox.googleapps.com/apps/messageheader/analyzeheader
https://mha.azurewebsites.net/



## Ip reverse lookup
https://ipinfo.io/

## Url Checker
https://urlscan.io/

## Malware sandbox 
 https://app.any.run/
 https://www.hybrid-analysis.com/
 https://www.joesecurity.org/


 ## Phishtool