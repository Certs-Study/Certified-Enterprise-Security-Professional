# Containers in AD

• Public Key Services container under ‘Configuration Naming Context’ contains all AD CS related containers.&#x20;

• Some of the interesting containers are:&#x20;

– Certificate Templates Stores certificate templates used by Enterprise CAs.&#x20;

– Certification Authorities Stores trusted root certificates. All certificates from this container are propagated to each client’s Trusted Root Certification Authorities through Group Policy.&#x20;

– Enrollment Services Stores Enterprise CA objects. Used by clients to locate Enterprise CAs. All certificates from this container are propagated to each client’s Intermediate Certification Authorities through Group Policy.&#x20;

– NTAuthCertificates Stores certificates for CAs that can issue smart card logon certificates and perform client private key archival. A smart card logon fails if there is no entry for the issuer here.
