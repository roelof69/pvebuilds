---
title: "Gem Choices"
description: "Mutation 10 Gem Choices."
lead: "Mutation 10 Gem Choices."
weight: 20
toc: true
---

## Armour Gems
The ideal gem loadout is 58.1% Elemental resist, via 8 mutation-specific gems with elemental protection on amulet or shield.

The majority of damage in mutations is elemental, so in order to perform consistently it's important to have a high base resistance against the mutation. 



### How the Fortify cap works in the game files

 Fortify is capped at 50% including gems, **except** if you achieve **equal to or greater than** 50.0% resistance.
 
 Achieving this breakpoint will nullify any fortify you apply towards the specific resistance, **gemstone dusts still apply**.
 ####
AF = Affixes (Gems, Oakflesh, Gemstone Dust); 

SE = Status Effects (Fortify applied actively via abilities or your healer); 

ABS = Total Absorption
```
if (AF >= 0.5 or AF <=-0.3) ABS = AF else ABS=MAX(-0.3,MIN(AF+SE,0.5))
```

### Ideal gems based on Elemental Absorption %
#### 58.1% Elemental Absorption
If you have an amulet or shield with **elemental protection** it's worth it to go above the 50% cap. Gemstone Dust also stacks with your 58.1% resistance, making this setup by far the most consistent. 

| Fortify 	|    Gem Choice   	| ElementalAbs 	| PhysicalAbs 	| TotalAbs 	|
|:-------:	|:---------------:	|:------------:	|:-----------:	|:--------:	|
|   35%   	|    8Specific    	|     58.1%    	|     35%     	|   46.6%  	|
|   35%   	|    8Specific    	|     83.1% w/Strong Gemstone Dust    	|     35%     	|   **59.1%**  	|
|   35%   	|    8Specific    	|     93.1% w/Powerful Gemstone Dust    	|     35%     	|   **64.1%**  	|
|   50%   	|    8Specific    	|     58.1%    	|     50%     	|   54.1%  	|
|   50%   	|    8Specific    	|     83.1% w/Strong Gemstone Dust   	|     50%     	|   **66.6%**  	|
|   50%   	|    8Specific    	|     93.1% w/Powerful Gemstone Dust    	|     50%     	|   **71.6%**  	|



#### Sub 50% Base Absorption
If you're unable to achieve the 50% breakpoint, you should pick gems depending on how much fortify you can reliably apply. Below is a table of the ideal gem choices for each fortify %.

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

