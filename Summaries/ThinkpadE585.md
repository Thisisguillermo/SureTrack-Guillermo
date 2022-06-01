# Thinkpad E585 possible fixes.

# Thinkpad sources.

https://forums.lenovo.com/t5/ThinkPad-11e-Windows-13-E-and/ThinkPad-E485-E585-Firmware-bug-ACPI-IVRS-table/td-p/4191484/page/11

https://forums.lenovo.com/t5/ThinkPad-11e-Windows-13-E-and/ThinkPad-E485-E585-Firmware-bug-ACPI-IVRS-table/td-p/4191484/page/12

---

 @unity98,

I compile from source straight from kernel.org.  They do make a handy tarball for download that you can compile wherever you want.  Here is a pretty good source to start with to give you an idea.

 

Don't get too excited about bug fixes based on Kenduro's reply.

 

@Kenduro,

I'm not sure what to say.  I haven't used iommu=xx for a long time.  I know I've adjusted IOMMU setting within my kernel so I imagine that's why I don't need it.  Not a big deal as it's an AMD issue.  

 

I don't have any suspend/wake issues.  I've been running the patch on rc2 for a couple of days and rc3 since last night.  Not one instance of failure to wake.  For today, that's nearly 24 hours.  I can't imagine any settings that I have kernel or bios that would effect that.  Come to think of it, the only settings I've changed are from a post of yours.  In the Thinkpad e485 bios 1.45 resume from suspend failed - Linux thread on post #4 you suggested disabling bluetooth and amd vmm.  I did that this weekend and that very well may have coincided with these other changes.  I dunno.


https://forums.lenovo.com/t5/Linux-Discussion/Thinkpad-e485-bios-1-45-resume-from-suspend-failed-Linux/m-p/4266963/highlight/true#M11986

https://forums.lenovo.com/t5/Linux-Discussion/Thinkpad-e485-bios-1-45-resume-from-suspend-failed-Linux/m-p/4266963/highlight/true#M11986

---

My config:

* BIOS: 1.32 (the keyboard patch)

* Kernel: 4.18.8 with Ubuntu sauces

* OS: Kubuntu 18.04

* GRUB Parameters:

    iommu=soft
    idle=nomwait (fix CPU freezing issue)
    ivrs_ioapic[33]=00:00.1 (microSD card reader fix)

* replaced Wifi card with the Intel one mentioned above

 

This is the most stable my machine has been running since I received it. No random hangs / crashes, suspend / wake works perfectly, bluetooth works after wake, etc. I've been using the compiled kernels from this repo that also include the new graphics drivers. Just a heads up for everyone.

 

I use this laptop for work so I can't really mess around with kernels too much. Uptime is currently >6  days.

---

Most of my aim has been to get the best possible idle power and this kernel boot param combination seems to do as well as is possible on 2500U.

"amdgpu.ppfeaturemask=0xffffbfff" seems to reduce idle power; additionally, I found that "iommu=pt" seems to use less power than "iommu=soft" but I haven't saved any W numbers.

---

Update - a so-far working combination?

 

    Bios 1.48
    Ubuntu 18.10 with kernel 4.20.8 from Ubuntu mainline builds https://kernel.ubuntu.com/~kernel-ppa/mainline/?C=N;O=D
    GRUB_CMDLINE_LINUX="amd_iommu_dump=1 ivrs_ioapic[32]=00:14.0 ivrs_ioapic[33]=00:00.1 psmouse.synaptics_intertouch=1 iommu=pt amdgpu.ppfeaturemask=0xffffbfff"
    Resume-from-suspend successful for 24h, including a long overnight suspend
    Idle power draw on low screen brightness about 5.4W (just idle terminals, no browser running)

I'm curious what idle power draw is for other boot options...

---

I had a machine with exactly the same CPU, a 2500U and had random CPU lockups. Now, with the E585 which also has the 2500U I have zero CPU lockups. The difference between both machines: the microcode. Thus, I guess these CPU issues could be adresses with microcode updates. With BIOS 1.48 I have microcode 0x810100b, the machine I had before had a different microcode. And it had freezes.... I just wonder, why had Ac** a different microcode? Don´t they get the same from AMD? Or do they add custom patches to the CPU microcode?

 

Concerning the amdgpu issue, I found some new option to play with : amd_iommu=force_isolation

 

from /proc/cmdline:
ivrs_ioapic[32]=00:14.0 ivrs_ioapic[33]=00:00.1 clocksource=hpet libata.force=1:nohrst amd_iommu=fullflush amd_iommu=force_isolation rcu_nocbs=0-7 pcie_aspm=off idle=nomwait

---

Doing some more research on the bluetooth for the intel 9260 card ive found that a similar bug has been listed

https://bugs.launchpad.net/ubuntu/+source/linux/+bug/1790454

 

One potential fix was mentioned

On machines with the Intel 8260 WiFi + Bluetooth combo adapter we are experiencing firmware loading failures on the Bluetooth adapter from time to time. Doing the loading operations in a mutually-exclusive fashion using a mutex avoids the problem.

 https://github.com/endlessm/linux/pull/424

 

The above might work for the 9260

 

edit***

Entering these commands gets bluetooth working for me

sudo rmmod btusb
sleep 1
sudo modprobe btusb


