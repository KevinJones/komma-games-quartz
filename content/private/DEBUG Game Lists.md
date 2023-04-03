---
title: "DEBUG Game Lists"
draft: true
tags:
- #rough 
---
```dataview
TABLE Developer, Publisher, release-date as "Release Date", oneliner as Desc, play-today as Play
FROM "gamerecs"
```
```dataviewjs
var data = dv.pages('"gamerecs"')
	.map(b => [b.file.link, b.developer, b.publisher, b["release-date"], b.oneliner, b["play-today"]]);

const table = dv.markdownTable(["Title", "Developer", "Publisher", "Release Date", "Desc", "Play"], data)

dv.paragraph(table);
```
Doesn't seem to render correctly on the web...

| Title                                                        | Developer         | Publisher         | Release Date     | Desc                                                         | Play                                                         |
| :----------------------------------------------------------- | :---------------- | :---------------- | :--------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| [Celeste](app://obsidian.md/gamerecs/Celeste.md)             | Maddy Makes Games | Maddy Makes Games | January 25, 2018 | Face your doubts and climb a mountain in this precise platformer. | [Steam](https://store.steampowered.com/app/504230/Celeste/) or [Switch](https://www.nintendo.com/games/detail/celeste-switch) |
| [Spelunky](app://obsidian.md/gamerecs/Spelunky.md)           | -                 | -                 | -                | -                                                            | -                                                            |
| [Super Metroid](app://obsidian.md/gamerecs/Super Metroid.md) | -                 | -                 | -                | -                                                            | -                                                            |
| [Tetris](app://obsidian.md/gamerecs/Tetris.md)               | -                 | -                 | -                | -                                                            | -                                                            |