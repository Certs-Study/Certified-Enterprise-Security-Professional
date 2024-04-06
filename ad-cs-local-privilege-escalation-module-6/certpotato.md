# 🟢 CertPotato

Virtual accounts (like apppool\defaultapppool) are used by services on a Windows machine. These are local managed service accounts.

### Virtual accounts

Virtual accounts allow Windows services to run without the need for a traditional user account or the ongoing management that such accounts necessitate. This simplifies administration and enhances security. For instance, IIS (Internet Information Services) uses the `apppool\defaultapppool` virtual account to isolate different web applications, reducing the risk of one compromised application affecting others.

These accounts:

* **Do not require a password.** Windows manages the virtual account's security credentials, eliminating the risk of password theft or misuse.
* **Automatically have access rights limited to the service they are associated with.** This means they cannot be used to gain access to other parts of the system inadvertently, providing a built-in principle of least privilege.
* **Can use network resources as themselves,** which is particularly useful for services that need to authenticate to another service or access network resources under their own identity, without needing to manage service account passwords.

To configure a service to use a virtual account, set the service's logon account to `NT SERVICE\<ServiceName>`. For IIS application pools, this is handled in the IIS management console, where each application pool can be configured to run under its own virtual account automatically.

### CertPotato

The CertPotato vulnerability presents a significant security risk, particularly as it exploits a particular aspect of virtual accounts to escalate privileges within a system. Specifically, this vulnerability allows an attacker to leverage virtual accounts in order to obtain the context of a machine account.&#x20;

By doing so, the attacker can execute operations or access resources that should only be accessible to that machine account, thereby circumventing established security measures and gaining unauthorized control or access to sensitive processes and data.&#x20;

Understanding and mitigating the risks associated with the CertPotato vulnerability is crucial for maintaining the integrity and security of affected systems.

We can request a TGT for the machine account without needing admin rights using the tgtdeleg trick.

```
Rubeus.exe tgtdeleg /nowrap
```

```
Rubeus.exe s4u /self /impersonateuser:Administrator /altservice:cifs/cb-webapp1.certbulk.cb.corp
/dc:cb-dc.certbulk.cb.corp /user:'cb-webapp1$' /rc4:B2FCBA1C3570AB9418994799B9BC985A /ptt
```

#### Mitigation Strategies for CertPotato Vulnerability

To secure systems against the CertPotato vulnerability and similar threats, organizations should consider implementing the following mitigation strategies:

1. **Regularly Update and Patch Systems**: Ensure that all systems are kept up-to-date with the latest security patches from software vendors.
2. **Restrict Machine Account Permissions**: Limit the permissions assigned to machine accounts to the minimum necessary for their intended operations.
3. **Monitor and Audit Account Activity**: Implement monitoring and auditing mechanisms to detect unusual activities that could indicate an exploitation attempt.
4. **Implement Least Privilege Principle**: Ensure that users and machine accounts operate under the principle of least privilege, accessing only the resources necessary for their tasks.
5. **Enhance Kerberos Security**: Configure Kerberos policies to restrict ticket delegation and enforce stricter authentication processes.

By applying these measures, organizations can significantly reduce the risk posed by the CertPotato vulnerability and safeguard their critical assets from unauthorized access.
