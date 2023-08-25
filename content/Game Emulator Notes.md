---
title: "Game Emulator Notes"
draft: true
tags:
- #rough 
- #sync
---

Standard disclaimer: this page will not tell you where to find ROMs or disc images for free. I want to encourage exploration, not stinginess. If you can afford to, you should always support game developers by buying an official release from a digital store (and also support the [Internet Archive](https://archive.org/) while you're at it.)

## Getting Started

You have two main options: downloading individual emulators per system or using [RetroArch](https://www.retroarch.com/), a multi-purpose front-end. I personally use RetroArch, but there are definitely reasons to dislike it. If you're new to this, I'd recommend starting with standalone programs like Nestopia, Genesis Plus GX, or Snes9x. You can use a launcher program like [LaunchBox](https://www.launchbox-app.com/) or [PlayNite](https://playnite.link/) if you want to keep games that use different emulators in one place.

A few notes about what to expect:
- Most 8-bit and 16-bit systems are pretty well-emulated. At the time, ports from one system to another are pretty different and were often licensed out to separate developers who had more experience with particular hardware. In my game recommendations I've listed the platform I prefer for these games where applicable.
- For MS-DOS, DOSBox has pretty nice integration with your host file system, though features like save states aren't possible. You'll also need to adjust the cycle speed to make sure the game doesn't run too slow or too fast. Efforts like [eXoDOS](https://kotaku.com/one-mans-quest-to-collect-every-classic-pc-game-in-exis-1839432488) can help you find working configurations for the games you want to play.
- Amiga emulators like [WinUAE](https://www.winuae.net/) are hard to set up but perform very well afterwards. You can often eliminate disk load times by using the WHDLoad version of a game. You can buy a license for the Amiga kickstart roms from [Amiga Forever](https://www.amigaforever.com/), which supports the continued health of the Amiga scene.
- The N64, Saturn, and original Xbox are notably difficult game consoles to emulate. Expect graphical glitches and crapshoot compatability. On the other hand, the Wii, Gamecube, PSP, and Dreamcast have better emulation than you might expect! The PS2 is somewhere in the middle, with software that runs some games quite well and other games poorly.
- You can run some early Windows games by installing Windows 3.1 in DOSBox, Windows XP in a virtual machine like VirtualBox, or WIndows 98 in PCem.
- Arcade games can often be emulated successfully using MAME, with the occassional subtle bug. Configuring analog control (e.g. steering wheels) for MAME is tough, though.
- **NTSC vs PAL:** With most game hardware made before 2000, the difference between the NTSC 60Hz and PAL 50Hz utilty frequency means that games play at different speeds. For most games, playing in the NA or JP regions will mean play is faster and smoother. For games developed in Europe, or ones that just seem unplayably fast, the PAL region will give you a better resolution and more appropriate gameplay.
- **Displays:** Today, almost all devices use a flat-panel display with square pixels. However, this wasn't always the case on older systems; they were usually stretched to fill a 4:3 CRT television. Think "blurry rectangle" rather than "sharp square". For example, the SNES's pixel blocks are not 1:1, but more like 8:7; slightly wider than tall. The 320x200 resolution of many DOS games was stretched vertically. If you don't like the sharp edges of pixels, you can get closer to an intended look by using shaders. Some good test cases:
	- The dithered waterfalls of *Sonic the Hedgehog* look closer to the intended transparency effect over composite video output, rather than RGB.
	- The user interface of *Wave Race* for the Game Boy should look translucent due to intentional ghosting, rather than flickering.
	- DOS games should not appear "widescreen". 

## The Browser Option

Thanks to the power of webassembly, there are some emulators that can run in web browsers, supported by non-commercial sites. Here are some reputable ones I've found.

- [Atari Mania](http://www.atarimania.com/about.html) lets you learn about games for the 2600, 5200, Jaguar, and other Atari platforms. Many 2600 games can be played in your browser here with a link to the Javatari emulator.
- The Internet Archive contains a section called [The Emulation Station](https://archive.org/details/emulation) which allows you to sample a variety of old games in your browser.

## The MiSTer Option

TODO

## Further Reading