# Begin of nmap
*nmap -sC (default script) -sV (service detection) -oA (save in all formats) 10.10.10.182*

## Port 88 = Kerberos
>
![Kerberos](https://www.manageengine.com/products/active-directory-audit/kb/images/event-4771-kerberos-authentication-illustration.jpg)
>
>
## Port 135 = Microsoft RPC
>
![Microsoft RPC](https://docs.microsoft.com/en-us/windows/win32/rpc/images/httprpc1.png)
>
>
# Enumerating RPC to identify usernames

# Setting up a bruteforce and creating a custom wordlist with hashcat

# Enumerating LDAP with LDAPSEARCH

# Discovering the cascadeLegacyPwd LDAP Attribute which has a password

# Using CrackMapExec to test the credential found in LDAP 

# Installing the latest CrackMapExec to gain access to the Spider_Plus Module

# Using the spider_plus module of CME (CrackMapExec) to crawl the SMB Share as R.Thompson

# Mounting the SMB Share as R.Thompson in order to view the files in Data share

# Discovering the VNC Install.reg file which contains an encrypted password

# Using Metasploit IRB to decrypt TightVNC's password

# Using the VNC Password to gain a WinRM Session to Cascade as s.smith discovering he is in the Audit Group

# Using DNSPY to decompile the CascAudit DotNet application 

# Setting a breakpoint in DNSPY where the password is decrypted and viewing the variable after it decrypts the pw

# Gaining e remote shell as ArkSvc to discover this user is in the AD Recycle Bin Group

# Viewing deleted Active Directory items to see the TempAdmin has the CascadeLegacyPwd field and discovering this is the PW for administrator