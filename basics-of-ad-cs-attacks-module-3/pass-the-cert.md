# 🟢 Pass the Cert

### PTC using Schannel

If PKINIT is not supported by the DC, LDAPS can be abused to Pass the Cert using the PassTheCert tool.

### Explanation of PTC using PKINIT

Pass-the-Cert (PTC) using PKINIT is a technique that involves the manipulation of the Kerberos Pre-Authentication process by using a certificate.&#x20;

PKINIT (Public Key Cryptography for Initial Authentication in Kerberos) is an extension of the Kerberos protocol that allows for the use of X.509 certificates for the initial authentication to the Kerberos Key Distribution Center (KDC), typically a Domain Controller (DC) in Windows environments.

In a PTC attack leveraging PKINIT, an attacker with access to a valid certificate and its private key, either through extraction from a compromised system or via other means, can authenticate as the legitimate user without needing the user's password.&#x20;

This is because the authentication process is based on cryptographic proof of possession of the private key associated with the submitted certificate.

This technique is particularly impact in scenarios where strong two-factor authentication mechanisms are bypassed, allowing an attacker to gain authenticated access to resources within an Active Directory environment.&#x20;

Understanding and mitigating the risks associated with PTC using PKINIT requires a combination of proper certificate management, monitoring of authentication logs for anomalies, and implementing controls to limit the misuse of certificate-based authentication.
