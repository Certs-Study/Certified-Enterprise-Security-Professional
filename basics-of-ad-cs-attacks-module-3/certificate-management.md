# Certificate Management

### Request Certificate

Request Certificate in pem format:

```
certify.exe request /ca:cb:ca.cb.corp\CB-CA /template:User
```

### Import Certificate

Import Certificate into User Certificate Store

```
certutil --user --importpfx C:\certs\studentadmin.pfx
```

### Export Certificate

Export Certificate from User Certificate Store using Certificate Serial:

```
certutil -user -exportpfx 5500000019b448b6ebb68c9b09000000000019 C:\certs\studentadmin.pfx
```
