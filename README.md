# Fix: Running Scripts Is Disabled on This System

## Error Message

> [!CAUTION]
> ```powershell
> .\Script.ps1 : File C:\Script.ps1 cannot be loaded because running scripts is disabled
> on this system. For more information, see about_Execution_Policies at
> https://go.microsoft.com/fwlink/?LinkID=135170.
> At line:1 char:1
> + .\Script.ps1
> + ~~~~~~~~~~~~~~~~~~~~~~
>     + CategoryInfo          : SecurityError: (:) [], PSSecurityException
>     + FullyQualifiedErrorId : UnauthorizedAccess
> ```

## Temporary Solution (For Current Session)

> [!NOTE] 
> If you’re only looking to run the script this one time, use the following command to allow it to run in the current PowerShell session:

> [!TIP]
> ```powershell
> Set-ExecutionPolicy -ExecutionPolicy Unrestricted -Scope Process
> ```

## Permanent Solution (For Current User)

> [!NOTE] 
> Alternatively, if you want to be able to run scripts freely on your system going forward, use the following command:

> [!TIP]
> ```powershell
> Set-ExecutionPolicy -ExecutionPolicy Unrestricted -Scope CurrentUser
> 
