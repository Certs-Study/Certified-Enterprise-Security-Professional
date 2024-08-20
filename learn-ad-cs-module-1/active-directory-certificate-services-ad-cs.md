---
description: >-
  Explore our comprehensive article on Active Directory Certificate Services (AD
  CS). Learn how AD CS enhances security and facilitates data management in
  network environments.
---

# Active Directory Certificate Services (AD CS)

### Terminology

> * **PKI** (Public Key Infrastructure) — a system to manage certificates/public key encryption
> * **AD CS** (Active Directory Certificate Services) — Microsoft’s PKI implementation
> * **CA** (Certificate Authority) — PKI server that issues certificates
> * **Enterprise CA** — CA integrated with AD (as opposed to a standalone CA), offers certificate templates
> * **Certificate Template** — a collection of settings and policies that defines the contents of a certificate issued by an enterprise CA
> * **CSR** (Certificate Signing Request) — a message sent to a CA to request a signed certificate
> * **EKU** (Extended/Enhanced Key Usage) — one or more object identifiers (OIDs) that define how a certificate can be used

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

### Understanding PKI and Related Terminology

#### **Public Key Infrastructure (PKI)**&#x20;

**Public Key Infrastructure (PKI)** is a critical component in securing communications across networks. It utilizes a pair of keys (public and private) for encryption and decryption, ensuring that only the intended recipient can read the message.&#x20;

PKI encompasses several elements and procedures for managing these keys, including the issuance, renewal, and revocation of digital certificates.

### **Active Directory Certificate Services (AD CS)**

**Active Directory Certificate Services (AD CS)** is Microsoft's implementation of PKI. It allows organizations to build their own public key infrastructure, managing certificates for users, machines, and applications within the Windows environment.&#x20;

AD CS can be integrated with Active Directory, offering a seamless and secure infrastructure management platform.

### **Certificate Authority (CA)**

A **Certificate Authority (CA)**, central to the PKI, is responsible for issuing digital certificates. These certificates are essential for establishing a digital entity's identity over the network.&#x20;

The CA verifies the certificate requester's credentials before issuance, ensuring authenticity.

An **Enterprise CA** specifically refers to a CA that is integrated with Active Directory (AD). This integration offers advanced features, such as the use of certificate templates, which streamline the certificate management process.

**Certificate Templates** contribute to the automation and standardization of certificate issuance.&#x20;

They define a set of policies and settings that determine the contents and characteristics of the certificates an enterprise CA issues, aiding in efficient certificate lifecycle management.

### **Certificate Signing Request (CSR)**&#x20;

A **Certificate Signing Request (CSR)** is a plea sent from an entity to a CA, asking for identity verification and certificate issuance.&#x20;

The CSR contains the requester's public key and identifying information, which the CA uses to create a certificate.

### **Extended/Enhanced Key Usage (EKU)**&#x20;

Lastly, **Extended/Enhanced Key Usage (EKU)** specifies the purposes for which the issued certificate can be used.&#x20;

Defined by object identifiers (OIDs), EKUs help in restricting a certificate's applications to ensure its use aligns with the organization's security policies.

Through understanding these components, organizations can effectively implement PKI to enhance their security posture, ensuring secure communications and safeguarding sensitive information across their networks.
