---
description: >-
  Explore our comprehensive guide on Containers in AD and gain an in-depth
  understanding of their role in domain structure, benefits, and management.
  Improve your AD knowledge today.
---

# Containers in AD

**Active Directory Certificate Services Containers:**

* **Certificate Templates:** Stores certificate templates utilized by Enterprise CAs for generating certificates.
* **Certification Authorities:** This container holds trusted root certificates ensuring security across the network. These certificates are automatically disseminated to each client’s Trusted Root Certification Authorities via Group Policy, establishing a base of trust.
* **Enrollment Services:** Focuses on housing Enterprise CA objects. It is instrumental for clients in finding Enterprise CAs. Similar to the Certification Authorities container, certificates here are also propagated to each client’s Intermediate Certification Authorities through Group Policy.
* **NTAuthCertificates:** A specialized container storing certificates from CAs authorized to issue smart card logon certificates and manage client private key archival. For a smart card logon to proceed successfully, the issuing CA’s certificate must be present in this container, acting as a critical security measure.

These containers play pivotal roles in the management and deployment of certificates within a network, ensuring authentication, authorization, and secure communication.
