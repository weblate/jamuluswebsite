---
layout: wiki
title: "Client Troubleshooting"
lang: "en"
permalink: "/wiki/Client-Troubleshooting"
---

# Troubleshooting
 {:.no_toc}

<details markdown="1">

<summary>Table of contents</summary>

* TOC
 {:toc}

</details>

### Don’t hear any sound/Others don’t hear you?

Start with the simple stuff: make sure your instrument/microphone and headphones are connected to the correct sockets. Make sure no other applications like your browser, video conferencing tool etc. is also using your sound card. You should shut those down when using Jamulus. If that all looks OK and the problem persists, it's likely there's an issue with your sound device settings. This will depend on your particular setup (platform, hardware, software and drivers), so it's best to ask on [the forums](https://github.com/jamulussoftware/jamulus/discussions) for guidance.

**Windows users (ASIO4ALL)**: If you’re using the ASIO4ALL driver have a look at the [ASIO4LL setup section](Installation-for-Windows#setting-up-asio4all)

### Not seeing the headphone or microphone you just connected to your PC?

Just restart Jamulus with your device plugged in. Jamulus currently doesn't show devices which were plugged in after the sound system was loaded. 

### Your sound is stuttering

Your audio device may not work with the buffer size you selected. Select a bigger buffer size in Jamulus's settings. If possible though, use another device, since large buffer sizes mean higher latency. 

### You all sound OK, but it's difficult to keep together

**If at all possible, DO NOT listen to your direct signal.** Make sure you are listening as much as you can to the sound of your own instrument/voice _coming back from the server_. This signal has you and your playing partners mixed together in sync, and will be the signal that your bandmates are hearing too. So listening to that means you will be in sync with each other (assuming you all have reasonably low latency). Note that if one or more musicians are not following this rule, they will slow down as they play or sing.

You can test whether you are hearing your signal correctly by doing the following:

1. Run Jamulus and connect to a server with a long ping time (greater than 200ms)
2. Clap your hands once (or play one short note on an instrument). You should hear the sound from the Jamulus server come back, but significantly delayed.
3. Click the "Mute" button under your Jamulus name/slider in the main Jamulus mixer window (**NOT** the "Mute Myself" button on the left).
4. Clap your hands again.

If you hear two claps after step 2, or any claps after step 4, then you are **not** obeying Rule Number One - you have your local audio enabled and should disable it. 

Exactly how you avoid listening to your direct signal will depend on your individual setup - your sound interface, mixing desk, headphone connection point, etc. For example, some audio interfaces have "monitor" buttons (turn these off), or similar options. **If you are still having problems**, try asking on the [forum](https://github.com/jamulussoftware/jamulus/discussions). 

Be aware that while listening to the server's signal will ensure you will be in sync with other musicians, you may also experience problems if your overall latency (indicated by the "Delay" light in Jamulus) is not green or at least yellow most of the time. Consult the [software manual](/wiki/Software-Manual) to understand how to adjust your setup to help with this.

### Can't work out your mic settings?

When using a microphone while playing your other instrument, you can use a stereo audio input signal in your settings where one channel is connected to the instrument and the other channel is connected to a microphone signal. On the microphone channel an optional reverberation effect can be applied.

### Buffer LEDs suddenly going red, outages, jittering, weird sounds?

The CPU in your computer may be having issues. Try not to have anything competing with Jamulus (like Zoom Meetings or Facebook live streams) on your machine. Or at least quit them while you're playing. Prevent things like virus scanners doing scans, or software updates happening, etc. Be aware that the reverb setting in Jamulus also uses more CPU the more reverb you have.

### Ping times and latency start well, then get worse, causing issues

This can indicate something else is competing with Jamulus on your network, so make sure nobody is watching HD Netflix movies or taking part in Zoom video conferences while you are playing. A more permanent solution for technically-minded users may be found by investigating [the issue of buffer bloat](https://www.bufferbloat.net/projects/bloat/wiki/) on their router and whether you can implement Smart Queue Management (SQM). [More details here](https://www.bufferbloat.net/projects/bloat/wiki/What_can_I_do_about_Bufferbloat/).

### Getting frustrated with software channels, audio routing, sample rates and more?

It's usually far easier and more reliable to have a [mixing desk](https://www.thomann.de/pics/bdb/191244/7355025_800.jpg) to connect your kit (instruments, mic, recorder etc.) and then send a simple stereo signal to your sound interface (be sure to listen to the resulting sound from the Jamulus server via your computer though!). The huge variety of possible hardware, software and instrument combinations means that setting up your sound card to work with your particular configuration can otherwise get complicated very fast.

### Somebody joining your jam and being too loud?

You can set your "New Client Level" to a low value (e.g. 10), or set the musicians you are playing with to "Solo" state (in the mixer panel on the right side). That way, either new entrants will be very quiet, or you won't hear them at all.

### Can't see the server you want to join?

First check that you have the right genre server selected in your Connection Setup window. Sometimes network issues mean your client won't list all the available servers. If you know the name of the server you want to join, you can [look up its IP address here](https://explorer.jamulus.io/). Enter the IP address in the "Server Name/Address" field in the Connect Setup window to connect to it.

### Not seeing a list of servers at all?

In the UK (and possibly other regions/routers) the Virgin Media Cable Internet Modem setting can cause an issue. "Block Fragmented IP Packets" should not be checked. For other routers/ISP, also try turning off SPI (Stateful Packet Inspection) and if that fixes it, you can make a judgment about whether to leave that off or not.

In some cases, it may be your ISP that is blocking your use of Jamulus. See the note on the [server troubleshooting page](Server-Troubleshooting#nobody-can-connect-to-my-server---but-i-can-connect-locally) about "Nobody can connect to my server"

### Trouble using Garageband (or other DAW) with Jamulus?

See [this forum discussion](https://sourceforge.net/p/llcon/discussion/533517/thread/d3dd58eedc/#b994)

### Using a Mac and your input is not heard?

(With thanks to [Mark Anthony De Souza](https://www.facebook.com/groups/619274602254947/permalink/765122847670121/?comment_id=765525034296569))

Maybe you did not answer "Yes" to the `"Jamulus wants to access your microphone"` challenge.  To fix this:
* Go to `Preferences` > `Security & Privacy` > `Privacy` tab
* Find `Microphone` on the left and then make sure `Jamulus` is enabled on the right-hand list

***

For anything else, please search or post on the [Discussion Forums](https://github.com/jamulussoftware/jamulus/discussions)
