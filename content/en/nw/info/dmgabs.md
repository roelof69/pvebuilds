---
title: "Damage Absorption"
description: "New World Damage Absorption"
lead: "Explanation of how damage absorption/mitigation functions"
weight: 10
toc: true
---

---

## How Fortify Cap Works

Each of your individual resistances are capped at 50%. Seen here in your inventory:<br><br>
<img src="https://i.imgur.com/UBokXGg.png"></img>
<br><br>
However, if you're able to achieve over 50% in this interface, via gems and protection perk, then the cap becomes the % displayed.
<br><br>
This means that if you have, for example, 50% Nature Resistance and you apply 30% Fortify:

- You cannot increase your Nature Resistance above 50%, so the 30% Fortify is wasted.
  
- 30% Fortify is applied to **all other resistances**, and is capped at 50% in each resistance.
  

---

### Damage Absorption Formula
Credit to <a href="https://discord.com/users/205096956941434880"><t>Mixed Nuts</t></a>.

-- This the best guess at the logic behind damage absorption in-game and is what the above calculator is based on.
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

## Absorption Calculator
The sheet for this calculator can be found [here](https://docs.google.com/spreadsheets/d/1dG5PGholXP_6kcKXk43Own0J5Q2LWktTknxIvmzkDc0/edit?usp=sharing) if you want to make a copy.



<div style="display:flex;height:770px;width:105%;overflow:hidden;">
<iframe width="100%" height="100%" style="margin-left:-48px;margin-top:-25px;" src="https://docs.google.com/spreadsheets/d/1dG5PGholXP_6kcKXk43Own0J5Q2LWktTknxIvmzkDc0/edit?usp=sharing?&amp;rm=minimal&amp;single=true&amp;headers=false&amp;"></iframe>
</div>

---
