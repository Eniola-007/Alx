# Mails sent from Exchange Online/GSuite to Gmail.com is marked as spam but not Outlook.com or Exchange Online or Gmail with Google workspace.

Blacklists are most commonly a collection of email or IP addresses which have been flagged for sending spam. If you are to send Bulk mail use a Bulk mail mailing service.  
Many email hosting providers will use these public blacklists as part of their overall efforts to limit the spam they receive to their network. They regularly undertake an IP blacklist check and block communications from IP addresses that are suspected of malicious activities. The blacklist itself is a list containing ranges of IP addresses that are blocked.  
Being blacklisted is triggered by a different of set criteria. For example, if a certain amount of spam traps are hit or suspected mail spam is received from a particular email/IP address within a certain time frame, an email provider like Google or Exchange will realise the IP address it comes from. In response to this, they’ll blacklist the IP address and any email sent from it will bounce back.  
  
If more than One Person in the Organization keeps sending Bulk mail and Admin doesn't take the Right Action by Educating them, the Entire Tenant either on Microsoft or Google workspace will be restricted from send mail over the internet. And if the user Account is compromised, be sure to change the password, apply policies and Ensure 2FA/MFA enabled.  
  
**Issue Description:**  
Mails sent from Exchange Online to [Gmail.com](http://Gmail.com) is marked as spam but not [Outlook.com](http://Outlook.com) or Exchange Online or Gmail with Google workspace.

**Troubleshooting steps:**  
Check the message Header for the Sending IP. You can always use Mxtoolbox([https://mxtoolbox.com/EmailHeaders.aspx](https://mxtoolbox.com/EmailHeaders.aspx)) or Microsoft Remote Connectivity Analyzer ([https://mha.azurewebsites.net/](https://mha.azurewebsites.net/)) to Analyze the message header.  
Check if the Sending IP is Blacklisted. If so Manually Whitelist the IP by going to the website that Blackisted the IP.

Also, Ensure you have SPF Record and DKIM Enabled. Check out the following link on Enabling DKIM [https://support.google.com/a/answer/180504?hl=en](https://support.google.com/a/answer/180504?hl=en) or [https://learn.microsoft.com/en-us/microsoft-365/security/office-365-security/email-authentication-dkim-configure?view=o365-worldwide](https://learn.microsoft.com/en-us/microsoft-365/security/office-365-security/email-authentication-dkim-configure?view=o365-worldwide) or use a DKIM Generator to generate the DKIM record and update DNS manager with the CNAME value.  
  
Note: You can always do check for blacklist, MX, SPF and DKIM lookup using [mxtoolbox.com](http://mxtoolbox.com)