# Extract the Private Key

```
$pw = ConvertTo-SecureString "password123" -AsPlainText -Force
$certificate = Get-ChildItem -Path cert:\CurrentUser\My\<thumbprint>
Export-PfxCertificate -Cert $certificate -FilePath user.pfx -Password $pw
```
