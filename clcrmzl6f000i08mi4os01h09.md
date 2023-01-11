# Gmail with Google workspace/Gsuite Unable to receive mails from Other Organization or Other mail provider e.g. yahoo.com,outlook.com etc.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1673437741455/52405b4a-5654-4d28-9daa-b0d63cebe078.png align="center")

Some Admins always forget to Update the Mail Exchange(MX) Record after moving to a new mailing service be it Gmail with Google workspace or Exchange Online. Hence, they won't be able to send to or receive from External Recipients.

All that is needed to be done is to go to the DNS manager and update the MX record accordingly and give it the right priority.  
  
Do follow the instructions below to setup MX record for Gmail with Google workspace;

1\. Sign in to your domain's account at your domain host (e.g. GoDaddy).  
2\. Locate the page for updating your domain's DNS records. The page might be called something like DNS Management, Name Server Management, or Advanced Settings.  
3\. Locate the MX records for your domain. You may already have one or more MX records. Delete any MX record not pointing to the Google server.  
4\. Change the existing MX records to point to Google mail servers by entering the MX record values below.

<table><tbody><tr><td colspan="1" rowspan="1"><p><strong>MX server address</strong></p></td><td colspan="1" rowspan="1"><p><strong>Priority</strong></p></td></tr><tr><td colspan="1" rowspan="1"><p><a target="_blank" rel="noopener noreferrer nofollow" href="http://ASPMX.L.GOOGLE.COM" style="pointer-events: none">ASPMX.L.GOOGLE.COM</a></p></td><td colspan="1" rowspan="1"><p>1</p></td></tr><tr><td colspan="1" rowspan="1"><p><a target="_blank" rel="noopener noreferrer nofollow" href="http://ALT1.ASPMX.L.GOOGLE.COM" style="pointer-events: none">ALT1.ASPMX.L.GOOGLE.COM</a></p></td><td colspan="1" rowspan="1"><p>5</p></td></tr><tr><td colspan="1" rowspan="1"><p><a target="_blank" rel="noopener noreferrer nofollow" href="http://ALT2.ASPMX.L.GOOGLE.COM" style="pointer-events: none">ALT2.ASPMX.L.GOOGLE.COM</a></p></td><td colspan="1" rowspan="1"><p>5</p></td></tr><tr><td colspan="1" rowspan="1"><p><a target="_blank" rel="noopener noreferrer nofollow" href="http://ALT3.ASPMX.L.GOOGLE.COM" style="pointer-events: none">ALT3.ASPMX.L.GOOGLE.COM</a></p></td><td colspan="1" rowspan="1"><p>10</p></td></tr><tr><td colspan="1" rowspan="1"><p><a target="_blank" rel="noopener noreferrer nofollow" href="http://ALT4.ASPMX.L.GOOGLE.COM" style="pointer-events: none">ALT4.ASPMX.L.GOOGLE.COM</a></p></td><td colspan="1" rowspan="1"><p>10</p></td></tr></tbody></table>

\*Please ensure the newly added MX records above have higher priority over any existing MX record, that way inbound emails sent to the domain can be routed to G-Suite Server for delivery.  
  
Check out this link for more info [Google Workspace MX record values - Google Workspace Admin Help](https://support.google.com/a/answer/174125?hl=en)  
  
**Note**:  
*It can take up to 72 hours for the new records to update through the system. During this time, mail sent to your domain might bounce. While there's no way to avoid email bouncing entirely, there are steps you can take to avoid it.*