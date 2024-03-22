# 🟢 CAs Info

Find CA inside the Domain

```
Get-ADObject -Filter * -SearchBase 'CN=Certification Authorities,CN=Public Key
Services,CN=Services,CN=Configuration,DC=cb,DC=corp’
```

```
ls 'AD:\CN=Certification Authorities,CN=Public Key
Services,CN=Services,CN=Configuration,DC=cb,DC=corp'
```

```
Get-ADObject -LDAPFilter '(objectclass=certificationAuthority)' -SearchBase
'CN=Configuration,DC=cb,DC=corp' | fl *
```

Enumerate CA

```
Certify.exe cas
```

Find Vulnerable CA Templates

```
Certify.exe find
```
