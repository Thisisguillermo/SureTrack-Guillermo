# Microsoft Defender

WD is no longer only signature based! All next gen protection capabilities like machine learning models are included with the free WD version. things that are only in the premium version have to do with hardening, enterprise features, reporting, EDR, automation & adv sandboxing.

regardless of what peopls choose, just remember that signature based detection just doesn't cut it anymore. Even with Microsoft Defender, you need to pay for the next gen (Advanced Threat protection) level to catch today's threats.

https://www.microsoft.com/security/blog/2019/06/24/inside-out-get-to-know-the-advanced-technologies-at-the-core-of-microsoft-defender-atp-next-generation-protection/

## Microsoft Defender tips:

For relatives that are more prone to installing junk software bundlers, Windows Defender has protections for it that are only intended for Enterprise customers.

However, you can force it on with this PowerShell:

`Set-MpPreference -PUAProtection enable`

And it does enable: Signature set for Potentially Unwanted Applications.

## Leveling up Windows Defender

https://jacksonvd.com/levelling-up-windows-defender/

## Security baseline (FINAL) for Windows 10 v1903 and Windows Server v1903

https://docs.microsoft.com/en-us/archive/blogs/secguide/security-baseline-final-for-windows-10-v1903-and-windows-server-v1903


## ConfigureDefender

ConfigureDefender is a small utility for configuring Windows 10 built-in Defender Anti-Virus settings. ConfigureDefender utility is a part of Hard_Configurator project, but it can be used as a standalone application (portable).

https://github.com/AndyFul/ConfigureDefender