---
title: "TitleHere"
draft: true
platforms:
- trs-80 CoCo
date-spec: y
tags:
- #gr-rpghm 
- #gr-real-time-rpg 
- #gr-fantasy 
- #gr-post-classical 
- #quartz-sync
---

(oneliner:: First-person, real time, fantasy maze dungeon.)

Developer:: DynaMicro
Publisher:: Tandy Corporation
Release Date:: 1982-01-01
Hours:: 0.5

*Daggorath* has a weird interface and is hard to play, but is also much creepier than it has any right to be. Your character's health is represented by a heartbeat that gradually speeds up when you exert yourself in combat. The halls you explore are dark and quiet, save for the scurrying of monsters. It's also notable just for being one of the first games that attempted to portray 3D space with real-time gameplay, especially for home computers.

Play Today:: [Web](https://daggorath.online/)

Gameplay tips:

You start with a sword and a torch that you'll need to use to tell what's going on.
- `P R SW` to **P**ull (with your **R**ight hand) the **SW**ord out of your backpack.
- `P L T` to Pull (with your Left hand) the **T**orch out of your backpack.
- `U T` to **U**se the Torch. This will let you see what's going on around you.

Move with the M commands `M, M B, M L,` and `M R`, and turn in place with the T commands `T L, T R, T A`. Climb ladders and enter holes with `C U` and `C D`.

Use `EXAMINE` to see the items on the floor and in your pack. Use `LOOK` to return to your normal view afterwards.

To do stuff with items, you'll need an empty hand. Use `S R` or `S L` to **S**tow an object from your hand into your backpack. You can then Get an object from the floor (for example, `G L T`) or Drop an object onto the floor.

To clarify, if you've got something in both hands, and you want to move something from the floor to your backpack, you should 
1. Optionally, `EXAMINE` to see what the item is.
2. Stow the thing in your right hand. `S R`
3. Get the item. If it is a torch, you'd do `G R TR`
4. Stow the new item. `S R`.
5. Pull the old item back out, e.g. `P R SW`
6. Optionally, `LOOK` to go back to the dungeon view.

Attack with the A command: `A R` to swing the sword. You can't see your health, but you'll want to run away from enemies if your heart is beating too fast. The only way to reduce your heartrate is by standing still. Your heart grows stronger by a little bit with every monster you defeat.

Once you get used to moving around and surviving your first few monster encounters, you'll want to start mapping out the dungeon and work your way to deeper levels. Save with `ZSAVE SAVEONE` and load with `ZLOAD SAVEONE`. 