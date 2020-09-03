# Windows Server

## Technet

https://social.technet.microsoft.com/wiki/contents/articles/default.aspx

## Windows troubleshooting

#### Nirsoft

https://www.nirsoft.net/


#### Windows Sysinternals

https://docs.microsoft.com/en-us/sysinternals/

#### Windows problem steps recorder

https://support.microsoft.com/en-us/help/22878/windows-10-record-steps

https://social.technet.microsoft.com/wiki/contents/articles/51722.windows-problem-steps-recorder-psr-quick-and-easy-documenting-of-your-steps-and-procedures.aspx

#### Windows Performance Toolkit

https://docs.microsoft.com/en-us/windows-hardware/test/wpt/

https://www.youtube.com/watch?v=6IXx7xx8t2Y&list=PLNY8tkEowMjQgwgcRv67itLoRKVOiBdh-&index=13

#### Using Process Monitor to capture system events and booting with process monitor

https://support.home.sophos.com/hc/en-us/articles/360000401146-Using-Process-Monitor-to-capture-system-events

## Run Commands

https://ss64.com/nt/run.html

## Windows Server downloads

### Windows Server 2019

https://software-download.microsoft.com/download/pr/17763.737.190906-2324.rs5_release_svc_refresh_SERVER_EVAL_x64FRE_en-us_1.iso

### Windows Server 2016

https://software-download.microsoft.com/download/pr/Windows_Server_2016_Datacenter_EVAL_en-us_14393_refresh.ISO

### Windows Server 2012 R2

http://download.microsoft.com/download/6/2/A/62A76ABB-9990-4EFC-A4FE-C7D698DAEB96/9600.17050.WINBLUE_REFRESH.140317-1640_X64FRE_SERVER_EVAL_EN-US-IR3_SSS_X64FREE_EN-US_DV9.ISO

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


## Configure Defender

ConfigureDefender is a small utility for configuring Windows 10 built-in Defender Anti-Virus settings. ConfigureDefender utility is a part of Hard_Configurator project, but it can be used as a standalone application (portable).

https://github.com/AndyFul/ConfigureDefender

# Protect your PC from potentially unwanted applications (Windows 10)
Windows Security has reputation-based protection that can help protect your PC from potentially unwanted applications. Potentially unwanted app blocking was first introduced in Windows 10 May 2020 update, and is turned off by default.

Turn it on in Microsoft Defender.
https://support.microsoft.com/en-us/help/4562299/protect-your-pc-from-potentially-unwanted-applications

# How to add web sites to “Trusted Sites” via GPO from DC installed IE10 or higher IE version
https://docs.microsoft.com/en-us/archive/blogs/asiatech/how-to-add-web-sites-to-trusted-sites-via-gpo-from-dc-installed-ie10-or-higher-ie-version

# Turning on network protection
https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/enable-network-protection

# Windows VHD

"This brings up an interesting question.

My company won't give me a newer laptop.  Could I make a VHD out of my work laptop and run it as a VM on a much more powerful computer?"

Generally yes. Keep in mind your PC has tons of junk drivers you’ll need to uninstall/remove from Autoruns later to improve performance.

https://docs.microsoft.com/en-us/sysinternals/downloads/disk2vhd

Note this is a transition of logical data into a VHD within a running system, Bitlocker and all that doesn’t matter.
If somebody is admin they are god.


# BIOS updates

See, what do I tell y’all? BIOS updates. Update your BIOS. As someone here once told me, “Absolutely no company releases new firmware updates for fun. If it’s public, there’s a very good reason.”
I updated Dell BIOS on thousands of systems in my helpdesk role