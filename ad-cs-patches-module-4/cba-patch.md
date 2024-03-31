# 🟢 CBA patch

The CBA patch hinders Subject AltName abuses such as ESC1, ESC2, ESC3 and breaks CA Configuration abuses like ESC6, ESC9, ESC10.&#x20;

• Before the Full Enforcement patch date (Nov 14, 2023 for now available as OOB update) the " key value in the HKEY\_LOCAL\_MACHINE SYSTEM CurrentControlSet Services Kdc Registry Subkey can be altered in 3 states to set Certificate-based Authentication checks.&#x20;

– **Disabled**: 0 ––> SID Mapping checks are disable

– **Compatibility**: 1 szOID\_NTDS\_CA\_SECURITY\_EXT is checked and validated if present, but if a strong mapping is not present authentication can still proceed but will be logged.&#x20;

– **Full Enforcement Mode**: 2 ––> strong SID mapping requirements in client certificates, and if not present authentication fails and will be logged.
