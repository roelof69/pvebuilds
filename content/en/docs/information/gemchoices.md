---
title: "Gem Choices"
description: "Mutation 10 Gem Choices."
lead: "Mutation 10 Gem Choices."
weight: 20
toc: true
---

## Armour gems
The ideal gem loadout is 58.1% Elemental resist, via 8 mutation-specific gems with elemental protection on amulet or shield.

The majority of damage in mutations is elemental, so in order to perform consistently it's important to have a high base resistance against the mutation. 



## How the fortify cap works

Each of your individual resistances are capped at 50%. Seen here in your inventory:<br><br>
<img src="https://i.imgur.com/UBokXGg.png"> 
<br><br>
However, if you're able to achieve over 50% in this interface, via gems and protection perk, then the cap becomes the % displayed.
<br><br>
This means that if you have, for example, 50% Nature Resistance and you apply 30% Fortify:

- You cannot increase your Nature Resistance above 50%, so the 30% Fortify is wasted.
  
- 30% Fortify is applied to **all other resistances**, and is capped at 50% in each resistance.
  

### Damage absorption formula
Credit to <a href="https://discord.com/users/205096956941434880"><u>Mixed Nuts</u></a>.

-- This the best guess at the logic behind damage absorption in-game.
<br>

- AF = Affixes (Gems)

- SE = Status Effects (Fortify via healer, abilities, oakflesh or gemstone dust)

- ABSVitals = Ward armour perks and potions

```
MIN(MAX(AF+SE,MIN(AF,-0.3)),MAX(AF,0.5))+ABSVitals
```
<br>

Put simply, your absorption is: **(AF + SE)** + ABSVitals

- **AF + SE** is capped at 50%, unless AF is over 50% as mentioned above.

<br>

---

## Ideal gems based on elemental absorption %
### 58.1% Elemental Absorption
If you have an amulet or shield with **elemental protection** it's worth it to go above the 50% cap. Ward potions also stacks with your 58.1% resistance, making this setup by far the most consistent. (Gemstone Dust & Oakflesh Balm are counted as fortify %)

| Fortify 	|    Gem Choice   	| ElementalAbs 	| PhysicalAbs 	| TotalAbs 	|
|:-------:	|:---------------:	|:------------:	|:-----------:	|:--------:	|
|   35%   	|    8Specific    	|     58.1%    	|     35%     	|   46.6%  	|
|   50%   	|    8Specific    	|     58.1%    	|     50%     	|   54.1%  	|



### Sub 50% Base Absorption
If you're unable to achieve the 50% breakpoint, you should pick gems based on how much fortify you can reliably apply. Below is a table of the ideal gem choices for each fortify %.

| Fortify 	|    Gem Choice   	| ElementalAbs 	| PhysicalAbs 	| TotalAbs 	|
|:-------:	|:---------------:	|:------------:	|:-----------:	|:--------:	|
|   10%   	| 6Specific,2Onyx 	|      46%     	|     15%     	|   30.5%  	|
|   20%   	| 5Specific,3Onyx 	|      50%     	|    27.5%    	|   38.8%  	|
|   30%   	| 3Specific,5Onyx 	|      48%     	|    42.5%    	|   45.3%  	|
|   35%   	| 2Specific,6Onyx 	|      47%     	|     50%     	|   48.5%  	|
|   40%   	|   4Opals,4Onyx  	|      50%     	|     50%     	|   50.0%  	|
|   50%   	|       N/A       	|      50%     	|     50%     	|   50.0%  	|



## Weapon Gems
### DPS
The ideal weapon gem for each build is listed alongside that build.

For all DPS it's ideal to use a Cut Pristine Opal **or** Diamond **unless** the following is true:


```
(30% - WPN%)/2 >= 15%
```
- 30% = The maximum % bonus any elemental type will do.
- WPN% = The % bonus your weapon does against the mobtype. [Found here](/docs/information/mobresists/)
- Divide by 2 as elemental gems convert half of your damage.
  
examples:

-- Hatchet vs Angry Earth = (30% - 20%)/2 = 5% (This is why Opal is better than Ruby for Genesis.)

-- Spear vs. Ancients = (30% - 0%)/2 = 15% (Topaz is worth using for the consistent uptime)


### Healer
Healers should have a Cut Pristine Diamond in their Lifestaff, and a mobtype weakness gem in their Void Gauntlet.

### Tank
Tanks should be using a Cut Pristine Carnelian in **both** weapons.

