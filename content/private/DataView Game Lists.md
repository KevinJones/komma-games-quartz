---
title: "DataView Game Lists"
draft: true
tags:
- #rough 
---

This is a list of queries.

## Complete Game Recommendation List

```typescript

const pages = dv.pages('"gamerecs"')
const data = pages
	.sort(b => b["release-date"])
	.map(b => [b.file.link, b.developer, b.publisher, b.hours, b["release-date"], b["play-today"]])
const count = data.length
const hrs = pages.map(b => b.hours).array().reduce((acc, obj) => acc + (obj || 0), 0)
const headers = ["File", "Developer", "Publisher", "Hours", "Release Date", "Play Today"]

// then render it as desired.
dv.table(headers, data)
dv.paragraph(`Totals: ${count} games, ${hrs.toFixed(1)} hours.`)
```
TODO: respect the formatting suggested by the date-spec field
```dataviewjs
let headers = ["File", "Developer", "Publisher", "Hours", "Release Date", "Play Today"];
let pages = dv.pages('"gamerecs"')
let data = pages
	.sort(b => b["release-date"])
	.map(b => [b.file.link, b.developer, b.publisher, b.hours, b["release-date"], b["play-today"]]);

dv.table(headers, data);

let count = data.length;
let hrs = pages.map(b => b.hours).array().reduce((acc, obj) => acc + (obj || 0), 0);
dv.paragraph(`Totals: ${count} games, ${hrs.toFixed(1)} hours.`)
```

## Lists that look for tags
- #gr-greatest-hits 
- #gr-hidden-gems 
- #gr-best-in-multiplayer 
- #gr-best-in-multiplayer or #gr-supports-multiplayer 

Gameplay
- #gr-2d-shooter 
- #gr-3d-shooter 
- #gr-shmup 
- #gr-platformer 
- #gr-fighting 
- #gr-brawler 
- #gr-racing 
- #gr-pure-adventure 
- #gr-puzzle 
- #gr-management-sim 
- #gr-vehicle-sim 
- #gr-real-time-strategy or #gr-real-time-tactics or #gr-turn-based-tactics or #gr-turn-based-strategy 
- #gr-4X 
- #gr-trad-roguelike or #gr-modern-roguelike 
- #gr-cardboard 

Profiles
- #gr-acrobat 
- #gr-gardener 
- #gr-slayer 
- #gr-sightseer 
- #gr-skirmisher 
- #gr-gladiator 
- #gr-ninja 
- #gr-bounty-hunter 
- #gr-architect 
- #gr-bard 

Settings
- #gr-ancient 
- #gr-post-classical 
- #gr-modern-history 
- #gr-contemporary 
- #gr-futuristic 
- #gr-space 

Themes
- #gr-horror 
- #gr-fantasy 
- #gr-crime-and-mystery 
- #gr-historical 
- #gr-sci-fi 

## Lists based on Date
- Vintage - everything before the NES's release in July 1983
- The 8-bit era - July '83 to Sep '87
- The 16-bit era - Oct '88 to Sep '93
- The Polygon era - Oct '93 to Sep '99
- Early 00s - Oct '99 to Sep '04
- Late 00s - Oct '04 to Sep '09
- Early 10s - Oct '09 to Sep '14
- Late 10s - Oct '14 to Sep '19
- Early 20s - Oct '19 to present

## RPG combo lists
- #gr-rpg per era
- #gr-rpg or #gr-rpghm per era
- #gr-action-rpg 
- #gr-real-time-rpg 
- #gr-turn-based-rpg 

## Lists based on platform
- nes
- sms
- tg16
- gen
- snes
- gb
- gg
- segacd
- 3do
- jaguar
- saturn
- ps1
- n64
- gbc
- dc
- ngpc
- ps2
- gc
- xbox
- gba
- Apple II
- Atari 8-bit
- Atari ST
- BBC Micro
- NEC PC-88
- ZX Spectrum
- Commodore 64
- MS-DOS
- Macintosh
- Commodore Amiga
- ds
- psp
- xb360
- ps3
- wii
- 3ds
- vita
- wiiu
- ps4
- xb1
- switch