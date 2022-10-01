---
title: "FAQ"
description: "Answers to frequently asked questions."
lead: "Answers to frequently asked questions."
weight: 10
toc: true
---
<!-- Twitch Embed Styling -->
<style>
    .hide {
        display: none
      }
      
      
      /* The following css just makes sure the twitch video stays responsive */
      #twitch,
      #twitch2 {
        border-radius: 0.25rem !important;
        z-index: 1000;
        position: fixed;
        bottom: 5px;
        right: 5px;
        outline: 2px solid #121212;
        width: 432px;
        height: 243px;
        overflow: hidden;
      }
      
      #twitch object,
      #twitch iframe,
      #twitch2 object,
      #twitch2 iframe {
        z-index: 1000;
        border-radius: 0.25rem !important;
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
      }
      @media screen and (max-width:600px) {
        #twitch,
        #twitch2 {
          width: 208px;
          height: 117px;
          bottom:75px;
        }
      }
    
      
</style>
<!-- Twitch Video Embed -->
<script src="https://player.twitch.tv/js/embed/v1.js"></script>

<div id="twitch" class="hide">
</div>
<div id="twitch2" class="hide">
</div>

<script>
  var options = {
    channel: "m11pve",
    width: 1280,
    height: 720,
    parent: ["pvebuilds.xyz"]
  };
  var options2 = {
    channel: "genedictb",
    width: 1280,
    height: 720,
    parent: ["pvebuilds.xyz"]
  };
  var player2 = new Twitch.Player("twitch2", options2);
  var player = new Twitch.Player("twitch", options);
  player.addEventListener(Twitch.Player.READY, initiate)
  player.addEventListener(Twitch.Player.OFFLINE, initiate2);

  function initiate() {
    player.addEventListener(Twitch.Player.ONLINE, handleOnline);
    player.addEventListener(Twitch.Player.OFFLINE, handleOffline);
    player.removeEventListener(Twitch.Player.READY, initiate);
  }

  function handleOnline() {
    document.getElementById("twitch").classList.remove('hide');
    player.removeEventListener(Twitch.Player.ONLINE, handleOnline);
    player.addEventListener(Twitch.Player.OFFLINE, handleOffline);
    player2.pause();
    player2.setMuted(true);
    player.setMuted(false);
    player.setVolume(0.1);
  }

  function handleOffline() {
    player.setMuted(true);
    document.getElementById("twitch").classList.add('hide');
    player.removeEventListener(Twitch.Player.OFFLINE, handleOffline);
  }
  function initiate2() {
    player2.addEventListener(Twitch.Player.ONLINE, handleOnline2);
    player2.addEventListener(Twitch.Player.OFFLINE, handleOffline2);
    player2.removeEventListener(Twitch.Player.READY, initiate2);
  }

  function handleOnline2() {
    document.getElementById("twitch2").classList.remove('hide');
    player2.removeEventListener(Twitch.Player.ONLINE, handleOnline2);
    player2.addEventListener(Twitch.Player.OFFLINE, handleOffline2);
    player2.setMuted(false);
    player2.setVolume(0.1);
  }

  function handleOffline2() {
    document.getElementById("twitch2").classList.add('hide');
    player2.removeEventListener(Twitch.Player.OFFLINE, handleOffline2);
    player2.addEventListener(Twitch.Player.ONLINE, handleOnline2);
    player2.setMuted(true);
  }
</script>


## Armour Gems
**What gems should I have on my armour?**

It depends on the amount of fortify you're applying, [see here for an explanation.](/docs/information/gemchoices/) 

For the open world and base expeditions, use Cut Pristine Onyxes.

## Weapon Gems
**What gems should I have on my weapons?**

See [here](/docs/information/gemchoices/#dps) for an explanation.


## Armour Perks
**What armour perks are ideal?**

The ideal 3 perk combo is: Ward+SkillPerk+Refreshing

Your armour should have at least Ward on all pieces.

## Jewellery Perks
**What are the best jewellery perks?**

DPS and Tanks should have:
|   DPS/Tank   	|      Perk 1      	|              Perk 2              	|                                Perk 3                               	|
|:-------:	|:----------------:	|:--------------------------------:	|:-------------------------------------------------------------------:	|
|  Amulet 	|      Health      	|       Elemental  Protection      	|                         Refreshing or Empowered                        	|
|   Ring  	|     Leeching     	| DamageType   (e.g. Slash Damage) 	| Refreshing=Hearty.  If you're **over** 150DEX, Refreshing is better. 	|
| Earring 	| Refreshing Toast 	|            Refreshing            	|             Purifying Toast=Beloved=Evasive >Regenerating            	|

Healers should have:
|  Healer 	|      Perk 1      	|        Perk 2        	|                      Perk 3                     	|
|:-------:	|:----------------:	|:--------------------:	|:-----------------------------------------------:	|
|  Amulet 	|      Health      	| Elemental Protection 	|               Refreshing>Fortified              	|
|   Ring  	|      Sacred      	|        Hearty        	|             Refreshing or DamageType            	|
| Earring 	| Refreshing Toast 	|      Refreshing      	| Healthy Toast=Beloved=  Evasive=Purifying Toast 	|

## Weapon Perks
**What perks should my weapons have?**

3 Perk BIS is subjective. 

Bane and DMGCON is recommended, partnered with Refreshing Move/Keenly Empowered/Mortal Empower/Mortal Refresh. 

**Refreshing Torrent is BIS on Hatchet.**