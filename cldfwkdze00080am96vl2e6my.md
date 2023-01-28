# Unable to Install Windows 10 on Windows 7 using Media Creation Tool  Error Code 0x80072f8f0-20000

A lot of users get the error above when trying to upgrade from Windows 7 or 8 to Windows 10.

![Image](https://filestore.community.support.microsoft.com/api/images/96ab9e7a-edc9-4206-bcbe-8c6311d60ca2?upload=true align="center")

**Resolution Step:**

1. Download and Install/Open/Run Microsoft EasyFix using this link [https://download.microsoft.com/download/0/6/5/0658B1A7-6D2E-474F-BC2C-D69E5B9E9A68/MicrosoftEasyFix51044.msi](https://download.microsoft.com/download/0/6/5/0658B1A7-6D2E-474F-BC2C-D69E5B9E9A68/MicrosoftEasyFix51044.msi)  
    Note: To add the DefaultSecureProtocols registry subkey automatically.In addition to the DefaultSecureProtocols registry subkey, the Easy fix also adds the SecureProtocols at the following location to help enable TLS 1.1 and 1.2 for Internet Explorer.
    
2. Enabling TLS 1.2 and 1.2 from the registry editor.  
    **Note:** Create the necessary subkeys for TLS 1.1 and 1.2; create the DisabledByDefault DWORD values and set it to 0 in the following locations:  
      
    **For TLS 1.1**
    
    Registry location: **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\SecurityProviders\\SCHANNEL\\Protocols\\TLS 1.1\\Client**  
    DWORD name: DisabledByDefault  
    DWORD value: 0  
      
    **For TLS 1.2**
    
    Registry location: **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\SecurityProviders\\SCHANNEL\\Protocols\\TLS 1.2\\Client**  
    DWORD name: DisabledByDefault  
    DWORD value: 0