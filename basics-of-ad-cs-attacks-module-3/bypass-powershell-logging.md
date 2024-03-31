# 🟢 Bypass PowerShell Logging

#### Bypass PowerShell Logging

When working with sensitive environments, or in situations where privacy and security are paramount, bypassing PowerShell logging becomes a critical operation. This ensures that the commands executed and their outcomes remain confidential, without leaving traces in system logs that could be accessed by unauthorized users or administrators.

**Running with Administrative Privileges**

To execute scripts with elevated privileges, ensuring they bypass PowerShell logging, you can use:

```plaintext
C:\ADCS\Tools> C:\ADCS\Tools\ObfuscatedTools\InviShell\RunWithPathAsAdmin.bat
```

This batch file elevates the privileges of the PowerShell session, allowing scripts to run with admin rights, which can include operations that modify system settings, alter logging configurations, or access restricted information.

**Running with Non-Administrative Privileges**

In cases where administrative privileges are not available or desired, the following command can be used to execute scripts in a manner that attempts to bypass PowerShell logging, without requiring elevated rights:

```plaintext
C:\ADCS\Tools> C:\ADCS\Tools\ObfuscatedTools\InviShell\RunWithRegistryNonAdmin.bat
```

This approach is suitable for environments where modifying system-wide configurations is not permitted, but the need to avoid logging for privacy or security reasons still exists.

**Quitting the Session and Cleaning Up**

After completing the required operations, it's essential to properly exit the session and perform any necessary cleanup activities to ensure no residual data is left that could indicate the operations performed:

```plaintext
C:\ADCS\Tools> exit
```

Exiting the session closes the PowerShell window and terminates the current scripts running, ensuring that no unnecessary processes remain active.

**Note:** Usage of these methods should be done with a thorough understanding of the security implications and compliance with applicable policies and regulations.
