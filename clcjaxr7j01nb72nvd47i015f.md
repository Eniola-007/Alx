# Unable to Send mail in Office 365 NDR "This message couldn't be delivered because the sending email address was not recognized as a valid sender..."

A lot of Microsoft Customers are not aware of Microsoft 365 message-sending limits [https://learn.microsoft.com/en-us/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits-1](https://learn.microsoft.com/en-us/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits-1). Hence, they use Exchange online in Microsoft 365 to Send bulk mail. As a result, the sender/affected user may be flagged as a Spam sender. In some cases, the affected user account may be compromised hence, the bad actor uses the account to send out Spam.

Instead of Microsoft blocking the tenant based on IP reputation, the affected Account is blocked. Below is the resolution.

**Issue Description:**  
Unable to Send mails  
"This message couldn't be delivered because the sending email address was not recognized as a valid sender. The most common reason for this error is that the email address is, or was, suspected of sending spam. Contact the organization's email admin for help and give them this error message."

**Resolution Step:**  
In the Microsoft 365 Defender portal at [https://security.microsoft.com](https://security.microsoft.com), go to **Email & collaboration** &gt; **Review** &gt; **Restricted users**. To go directly to the **Restricted users** page, use [https://security.microsoft.com/restrictedusers](https://security.microsoft.com/restrictedusers).

1. On the **Restricted users** page, find and select the user that you want to unblock by clicking on the user.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1672935240853/302515f6-b488-423e-a691-b3a2b2743ba0.png align="center")
    
2. Click the **Unblock** action that appears.
    
3. In the **Unblock user** flyout that appears, read the details about the restricted account. You should go through the recommendations to ensure you're taking the proper actions in case the account is compromised.
    
    When you're finished, click **Next**.
    
4. The next screen has recommendations to help prevent future compromise. Enabling multi-factor authentication (MFA) and resetting the password are a good defense.
    
    When you're finished, click **Submit**.
    
5. Click **Yes** to confirm the change.
    
    **Note**
    
    Under most circumstances, all restrictions should be removed from the user within one hour. Transient technical issues might cause a longer wait time, but the total wait should be no longer than 24 hours.