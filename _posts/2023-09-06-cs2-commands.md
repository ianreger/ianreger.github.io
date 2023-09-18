---
layout: post
title: "CS2 Commands"
date: 2023-09-06 12:00:00 -0500
categories: [CS2,counter-strike]
tags: [binds,commands,csgo,cs2,jumpthrow] #all tags MUST be lowercase
---

### TLDR:

#### Practice

sv_cheats 1

bind n noclip

changelevel de_example


#### ETC.

bind X "say Your Message"

## PERFORMANCE

### cq_netgraph 1

Displays information about your latency in the top right corner of the game screen. Although, this is not as detailed as it was in CS: GO. You can use cl_showfps 2 as an alternative if you want the classic CS: GO netgraph.

### cl_showfps 1

This command will display a live FPS (frames per second) on screen, so you can see how well your system is holding up with CS2. You can also do showfps 2, 3, 4, and 5, for more information.

### voice_scale 0.5

Using the voice scale command, you can alter the volume of your teammates voice chat. This is a scaleable command, meaning you can increase or decrease the number at the end of the command, from 0-1.

### fps_max 0-999

This will set the FPS of the game. 0 being infinity, and 999 being the highest. 

## Practice Commands

### sv_cheats 1

The cheats command is not actual cheats, don’t worry. It simply allows you to override some of the basic limitations of regular matchmaking, so you’ll need it for some of the following commands.

### noclip

If you want to fly around the map and ‘clip’ through walls, no clip will let you do just that. You can also bind this to a key to have noclip on command. For example: bind n noclip – this will bind noclip to the alt key.

### sv_infinite_ammo 1

This command will give you infinite ammo in all weapons and grenades too. However, you can actually select this option on the left-hand side of the menu when launching a practice competitive map now.

### mp_respawn_on_death_ct 1;mp_respawn_on_death_t 1

This command will instantly respawn you if you die.

### mp_roundtime 60

This will give you an hour of time to practice without any round interruptions.

### mp_buytime 60000;mp_buy_anywhere 1;mp_maxmoney 65535;mp_startmoney 65535

This will allow you to buy weapons at any time, and at any location on the map. The money commands will make sure you have enough cash to do so.

### mp_restartgame 1

Sometimes, you’ll need to restart the game to make the commands above take effect, and you can do this with the restartgame command.

### changelevel [map code] 

example code: de_cache. If you want to quickly change maps in a practice server, use this command. For defuse maps, the code will also be de_[name]. For example, inferno is de_inferno.

### sv_rethrow_last_grenade

Throws the last nade thrown by whoever entered the command. Useful to see where flashes will pop or HEs will land. 

## CS2 bot commands

### bot_kick

This command will instantly kick all bots from the server.

### bot_add

If you feel bad and want to bring the bots back, use this command.

### bot_place

Adds a bot exactly where you are looking.

### bot_stop 1

Immediately stops all bots moving. You can also make them move again by changing 1 to 0.

### bot_mimic 1

This command will allow you to move the bot(s) around by having them mimic your inputs. Change to 0 to stop them.