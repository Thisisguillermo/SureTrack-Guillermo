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

## Deep Learning Super Sampling (NVIDIA)

 Deep Learning Super Sampling (DLSS)

 https://www.nvidia.com/en-us/geforce/news/nvidia-dlss-your-questions-answered/

https://www.nvidia.com/en-us/geforce/news/nvidia-dlss-2-0-a-big-leap-in-ai-rendering/

## DPC Latency

DPC (Deferred Procedure Call) is the operation that Windows uses to assign a priority to processes/drivers that run simultaneously in the same system. If processes that are involved in streaming audio aren't assigned high enough priority then various issues can occur since the audio will not be streamed correctly in 'real-time'. These can include pops/clicks, 'glitchy' audio and device disconnections.

A common cause for DPC latency is out of date device drivers and Windows processes that are not optimised correctly. Many processes/drivers are involved in streaming audio and many other processes/drivers can cause interruptions in the audio stream.

To analyse whether DPC latency could be the cause for any pops, clicks or disconnections you might be experiencing you can run the following software tool: Latency Mon (Windows 7 and later).

https://support.focusrite.com/hc/en-gb/articles/208360865-Troubleshooting-DPC-latency


## Suggest a laptop laptops

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
