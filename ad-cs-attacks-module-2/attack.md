---
description: >-
  Explore the intricacies of the Attack AD CS in this comprehensive article.
  Uncover the techniques, threats, and defense strategies against this
  cybersecurity concern.
---

# Attack

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

&#x20;

### Enumeration

<table><thead><tr><th>Technique ID</th><th width="401">Description </th><th data-hidden></th></tr></thead><tbody><tr><td>Enumeration </td><td>Enumerate if AD CS is present in the target environment, available templates and misconfigurations.</td><td></td></tr><tr><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td></tr></tbody></table>

### Local Privilege Escalation

<table><thead><tr><th>Offensive Technique ID</th><th>Description</th><th data-hidden></th></tr></thead><tbody><tr><td>CertPotato</td><td>Abuse virtual and network service accounts (authenticates as machine account in domain) to escalate privileges to local system</td><td></td></tr><tr><td></td><td></td><td></td></tr></tbody></table>

### Theft and Collection

<table><thead><tr><th>Technique ID</th><th>Description</th><th data-hidden></th></tr></thead><tbody><tr><td>THEFT1</td><td>Exporting certificates and their private keys using Window’s Crypto APIs</td><td></td></tr><tr><td>THEFT2</td><td>Extracting User certificates and private keys using DPAPI</td><td></td></tr><tr><td>THEFT3</td><td>Extracting Computer certificates and private keys using DPAPI</td><td></td></tr><tr><td>THEFT4</td><td>Theft of existing certificates on disk</td><td></td></tr><tr><td>THEFT5</td><td>Using the Kerberos PKINIT protocol to retrieve a User/Computer account’s NTLM hash</td><td></td></tr></tbody></table>

### Local Persistence

<table><thead><tr><th>Technique ID</th><th>Description</th><th data-hidden></th></tr></thead><tbody><tr><td>PERSIST1</td><td>User account persistence using new certificate requests</td><td></td></tr><tr><td>PERSIST2</td><td>Computer account persistence using new certificate requests</td><td></td></tr><tr><td>PERSIST3</td><td>User/Computer Account persistence by certificate renewal before expiration</td><td></td></tr></tbody></table>

### Domain Privilege Escalation

In Active Directory Certificate Services (AD CS), privilege escalation typically involves exploiting vulnerabilities or misconfigurations within the certificate authority (CA) structure or its deployment.

Techniques for escalation can range from intercepting and modifying certificate signing requests (ESCs 1-3) to leveraging flaws in CA security practices or protocols (ESCs 4-11), such as the notable Certifried vulnerability CVE-2022-26923.&#x20;

This particular exploit allows attackers to gain higher privileges within the domain by crafting malicious certificate requests.&#x20;

Understanding and mitigating these vulnerabilities is crucial for maintaining a secure AD CS environment.

<table><thead><tr><th>Technique ID</th><th>Description</th><th data-hidden></th></tr></thead><tbody><tr><td>ESC1</td><td></td><td></td></tr><tr><td>ESC2</td><td></td><td></td></tr><tr><td>ESC3</td><td></td><td></td></tr><tr><td>ESC4</td><td></td><td></td></tr><tr><td>ESC5</td><td></td><td></td></tr><tr><td>ESC6</td><td></td><td></td></tr><tr><td>ESC7</td><td></td><td></td></tr><tr><td>ESC8</td><td></td><td></td></tr><tr><td>ESC9</td><td></td><td></td></tr><tr><td>ESC10</td><td></td><td></td></tr><tr><td>ESC11</td><td></td><td></td></tr><tr><td>Certifried CVE-2022-26923</td><td></td><td></td></tr></tbody></table>

### Domain Persistence

Domain persistence within Active Directory Certificate Services (AD CS) can be achieved through several methods involving the exploitation of certificate authority (CA) mechanisms.&#x20;

Techniques include forging domain certificates by obtaining stolen CA Root certificates and private keys (DPERSIST1), or by leveraging stolen external Trusted Root certificates and private keys after adding them to the root or NTAuthCA certificates container (DPERSIST2).&#x20;

Additionally, persistence can be secured by backdooring the CA server utilizing malicious misconfigurations, similar to those described in ESC4 (DPERSIST3).&#x20;

These methods ensure sustained unauthorized access to the domain, enabling attackers to maintain a foothold within the environment without immediate detection.

<table><thead><tr><th>Technique ID</th><th>Description</th><th data-hidden></th></tr></thead><tbody><tr><td>DPERSIST1</td><td>Forge ANY domain certificate using stolen CA Root certificate and private keys</td><td></td></tr><tr><td>DPERSIST2</td><td>Forge ANY domain certificate using stolen external Trusted Root certificate and private keys (added root/ NTAuthCAcertificates container)</td><td></td></tr><tr><td>DPERSIST3</td><td>Backdoor CA server using malicious misconfigurations like ESC4 that can later cause a domain escalation</td><td></td></tr></tbody></table>

### Cloud Privilege Escalation and Persistence



<table><thead><tr><th>Technique ID</th><th>Description</th><th data-hidden></th></tr></thead><tbody><tr><td>Trust abuse Enterprise CA and Azure AD Certificate Based Authentication</td><td><p>A compromised Certificate Authority trusted by an Azure AD tenant enables forging certificates and impersonating any user in the target tenant. </p><p>This results in privilege escalation to the tenant if the user has administrative roles assigned to the tenant and persistence as long as the certificate doesn’t expire. </p></td><td></td></tr><tr><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td></tr></tbody></table>
