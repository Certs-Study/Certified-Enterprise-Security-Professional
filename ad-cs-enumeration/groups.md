# Groups

Here I am focusing on Enumeration related to AD CS&#x20;



```
certipy find -u 'rfs@ad-attacks.com' -p <password> -dc-ip <DC_IP> -vulnerable -enabled
```

### Cert Publishers Group

```
net group "Cert Publishers" /domain
```

```
crackmapexec ldap 'domaincontroller' -d 'domain' -u 'user' -p 'password' -M adcs
```
