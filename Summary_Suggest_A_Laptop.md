# Suggest a laptop

## Frametimes/framepracing

Frame pacing

*Have you ever played a game where there was a huge spike in graphical demand and your fps dropped sharply
that second or two when the drop occurs and your game looks like the stuttering incarnate*

that happening over and over is what bad frame pacing looks like

frametimes are the time inbetween frames
if you are doing 60fps, you're getting frames on a 16.67ms time interval
there's no "fix with trial and error", there is "AMD needs good RAM or a hacked BIOS and enthusiast-level tweaking"

[![AMD-frame-pacing.png](https://i.postimg.cc/GhRkKVhj/AMD-frame-pacing.png)](https://postimg.cc/G9M8hMDB)

Do you see the spiking green graph on the bottom right?
That's AMD mobile
those are the times inbetween frames

Frametimes are the time inbetween frames
if you are doing 60fps, you're getting frames on a 16.67ms time interval

### Consistent frame pacing

every 16.67ms you get a new frame, for 60fps
at 120fps that's every 8.33ms
6.8ms at 144fps
33.33ms at 30fps
when you have consistent frame pacing, it means that the frames come in proper timing
when your frame pacing is inconsistent, it means that some frames come too fast and then others come too slow
you're still getting 60 frames within a 1 second time window
however 2 frames might come at you as if you had 120fps
then the following 3 frames come at you as if you were at 30
so your game looks stuttery and in general not a fun experience to watch

### AMD reliance on RAM (AMD's multi-CCX CPU )

because AMD is SO reliant on low latency with RAM
AMD's CPU's inter-CCX latency is reliant on infinity fabric and RAM latency
if you spiked intel's latency high like AMD's you might start seeing similar issues
but intel doesn't have those issues to begin with
also

## RAM Performance

Because AMD CPUs on mobile for gaming are inferior to intel because nobody sells them with good RAM or decouples the IF from RAM for lower latency

AMD needs low latency

When a program is asking for something
it's better to finish it in 1 cycle over 2
what if 3200Mhz can finish a request in 1 cycle and 2133Mhz needs 2 cycles?
3200MHz at a latency of 22 cycles to churn out the answer is still "faster" than 2133MHz doing two cycles for a total of (15 x 2) 30
so in terms of RAM performance overall, higher speed is better even if latency is the same
that said
since AMD is so damn reliant on latency for smoothness and generally a good time when gaming
because the latency is consistently high, it's just a worse experience overall

higher speed at same latency is better than lower speed
CL22 3200MHz will function better than 2666 cl19
HOWEVER
they both are trash
they're JEDEC timings


## From d2

I don't think a single AMD laptop is worth wholeheartedly, no-caveat recommending to anyone for gaming
will a lot of people not notice? Maybe not even play games that use the CPU enough to make the problem show up?

it's less of a problem on the desktop systems because they have cheap good RAM
and better motherboards with tweaking options open
but on laptops you don't have the choice
and everyone is just checking "fps" and not "frametime pacing"
digital foundry checked frametime pacing and reported the stutter and bad pacing
which is why that screenshot exists
the simple fact of the matter is
the people who DO test these things (like Gamer's Nexus) don't give a toodle do about laptops
and don't test them
so there is very little information about them
and I mean if you're on a situation where anything is an upgrade obviously it'll be an improvement... but uhh
if you're asking me "why only this model and not this other model"

## Business Notebooks

- Longer support for BIOS updates
- Better/Stronger chassis
- Parts are far more longer available
- better warranties
- Some times better processors with Vpro or whatever

## Intel Iris Xe G7 can run GTA V at 1080p 60 FPS on normal settings, is roughly on par with the Radeon RX Vega 8 and GeForce MX250

https://www.notebookcheck.net/Intel-Iris-Xe-G7-can-run-GTA-V-at-1080p-60-FPS-on-normal-settings-is-roughly-on-par-with-the-Radeon-RX-Vega-8-and-GeForce-MX250.494333.0.html

# NVIDIA

Titan Drivers are a bridge between the overpriced quadro cards and geforce cards
and allow the titan cards to perform better
there is 0 actual hardware difference in every titan post the original Kepler Titan and Titan Black cards
But since the 3090 doesn't have access to Titan drivers, it's LITERALLY just an expensive gaming card

As of Ampere the Quadro/Tesla branding differentiation doesn’t even exist anymore 
It’s just RTX Axxx now
RTX A6000 is the only full GA102
Also it has 48GB of G6 mem
Since G6X isn’t dense enough

## Deep Learning Super Sampling (NVIDIA)

 Deep Learning Super Sampling (DLSS)

 https://www.nvidia.com/en-us/geforce/news/nvidia-dlss-your-questions-answered/

https://www.nvidia.com/en-us/geforce/news/nvidia-dlss-2-0-a-big-leap-in-ai-rendering/

## DPC Latency

DPC (Deferred Procedure Call) is the operation that Windows uses to assign a priority to processes/drivers that run simultaneously in the same system. If processes that are involved in streaming audio aren't assigned high enough priority then various issues can occur since the audio will not be streamed correctly in 'real-time'. These can include pops/clicks, 'glitchy' audio and device disconnections.

A common cause for DPC latency is out of date device drivers and Windows processes that are not optimised correctly. Many processes/drivers are involved in streaming audio and many other processes/drivers can cause interruptions in the audio stream.

To analyse whether DPC latency could be the cause for any pops, clicks or disconnections you might be experiencing you can run the following software tool: Latency Mon (Windows 7 and later).

https://support.focusrite.com/hc/en-gb/articles/208360865-Troubleshooting-DPC-latency


## Core parking

 CPU Core parking is a feature that was introduced in Windows Server 2008 R2. The processor power management (PPM) engine and the scheduler work together to dynamically adjust the number of cores that are available to run threads. The PPM engine chooses a minimum number of cores for the threads that will be scheduled. Cores that are parked generally do not have any threads scheduled, and they will drop into very low power states when they are not processing interrupts, DPCs, or other strictly affinitized work. The remaining cores are responsible for the remainder of the workload. Core parking can potentially increase energy efficiency during lower usage.

The problem with Windows way of core parking is lack of flexibility since by default you are given very few options for setting Core parking index on your machine


https://coderbag.com/programming-c/disable-cpu-core-parking-utility
https://docs.microsoft.com/en-us/windows-hardware/customize/power-settings/static-configuration-options-for-core-parking
https://superuser.com/questions/1435110/why-does-windows-10-have-cpu-core-parking-disabled

## Suggest a laptop laptops

https://docs.google.com/spreadsheets/d/1ssjkMTjjfF_W7SbTrK_vhYycuc3a0u0vyjl0xdDdThA/edit#gid=799629507

600 to 900 USD

- Acer Swift 3 with Ryzen Processors
- Lenovo Ideapad 5 15
- Hp Envy x360.

1600 - 2000 USD

- Lenovo ThinkPad T14 AMD (Check Lenoovo !perks)

https://www.notebookcheck.net/HP-ProBook-x360-435-G7-laptop-review-AMD-Ryzen-also-shines-in-the-business-convertible.494446.0.html


## Laptop info

Dell Precision 5000 series based on Dell XPS line
https://www.notebookcheck.net/Dell-Precision-5750-Workstation-Review-The-XPS-17-For-Professionals.491576.0.html

Dell Precision 7xxx series

Are better, with better build quality and better qa than 5000 series
# Suggest a laptops keyboard differences

http://www.notebookreview.com/feature/laptop-keyboards-explained-best-worst-keyboard-tech/

# Televisions and monitors

### 120hz games 2020 December

- Devil May Cry 5
- Dirt 5
- Call of Duty Cold War
# Intel

## Chipsheet

https://docs.google.com/spreadsheets/d/1zF-ULKS3rAynQgaNPXbWZkRuZ2mU7dBHK9K6hz4_GBQ/edit#gid=151091225
## Intel 11th gen

11 is... a real big complex bag to be honest
intel being fuckfaces that they are
they technically have 11th gen H-series chips coming out, but they're a subset of them that they call H35
in reality they're just the low-power productivity "formerly known as U-series" chips, given a more generous power envelope
more importantly, they top out at quad-core
per-core they're still definitely a fair bit better than the 9300H/10300H
but they're still going to be thread-starved for AAAs that scale wide
and they're no successor to the 9750H/10750H and above
## Intel-U

Intel's -U chips (eg i5-8250U) are 15 Watt chips made for basic functionality like word processing, video watching, etc. The laptops they come in have crippled them with low power limits or thermal design, to the point that they cannot hold (or often even approach)  their listed "up to" clockspeeds outside of short bursts, regardless of whether it's i3-, i5- or i7-series. What does this mean?
- Most benchmarks are short duration and only measure burst performance; they are unrealistically optimistic.
- Slim/light "premium" ultrabooks often have worse thermals and thus perform particularly badly.
- Power, thermals, and core count are more important to performance than i5 or i7 branding.

# Issues

Unfortunately, popular ThinkPad models produced between 2017 and 2020 that may have been recommended to members here are subject to potential USB C port failure thanks to defective Thunderbolt controllers. Some of these models include the T480, T490, X1 Carbon and Yoga, P51 to P53. USB C port failure may take the form of BIOS errors or system hangs, docking stations not being recognized, or being unable to charge the computer with the stock charger.
To prevent USB C failure or to potentially fix it, download the driver package and firmware package for your machine here: https://lnv.gy/2NVb01z
It takes approximately 3 to 5 minutes to properly install both pieces of software. If any persistent issues continue, contact Lenovo customer support.

Do you have problems with an AMD iGPU and a Nvidia dGPU? Like the garbage ASSUS TUF FX505? If you are having problems with driver installs, make sure that you have properly done the following things:
- Did you use DDU in Safe Mode to clean BOTH Nvidia and AMD GPU drivers?
- Did you install AMD iGPU drivers before Nvidia dGPU drivers?
- Did you use known-safe/working drivers, not just "the latest"?
- If the above failed, have you tried some modified drivers from laptop2go.com? To install these you must perform an advanced reboot and boot with Driver Signature Enforcement disabled (you can google how to do this from howtogeek and you'll get a great guide)
- If all else has failed, have you tried reinstalling the operating system to see if the drivers might finally actually work then?

Once all of the above has been completed, if you are unable to rectify the issue, please consider returning your laptop piece of shit and getting something at least somewhat resembling a functional unit.

# MSI Fan

MSI Silent Option allows proper fan control without any of the bloat/throttle that Dragon Center may introduce. the link to the information and download thread is here: https://forum-en.msi.com/index.php?topic=255972.0 (Please note that the fanspeeds go above 100% in Silent Option, and "Cooler Boost" from Dragon Center is equivalent to 150% in Silent Option)
