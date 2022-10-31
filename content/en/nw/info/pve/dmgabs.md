---
title: "Damage Absorption"
description: "New World Damage Absorption"
lead: "Explanation of how damage absorption/mitigation functions"
weight: 70
toc: true
---

---

## How The Fortify Cap Works

Each of your individual resistances are capped at 50%. Seen here in your inventory:<br><br>
<img src="/images/_etc/iceresistsAF.png"></img>
<br><br>
However, if you're able to achieve over 50% in this interface, via gems and protection perk, then your cap is set to the % displayed.
<br><br>
This means that if you have, for example, 52% Ice Resistance and you apply 30% Fortify:

- Your Ice Resistance is set to 52%

- You cannot increase your Ice Resistance above 52%, except via more gems, so the 30% Fortify is wasted.
  
- 30% Fortify is applied to **all other resistances**, and is capped at 50% in each resistance.
  

---

### Damage Absorption Formula
Credit to <a href="https://discord.com/users/205096956941434880" target="_blank"><t>Mixed Nuts</t></a>.

-- This the best guess at the logic behind damage absorption in-game and is what the below calculator is based on.
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
<style>
.desktop {
display:flex;
width:105%;
overflow:hidden;

}
.desktop iframe{
margin-left:-46px;
margin-top:-24px;
margin-bottom:-195px;
height:1000px;
overflow-x:hidden; 

}
@media(max-width: 775px) {
  .desktop {
    display: none;
  }
}
  @media(min-width: 776px) {
  .mobile {
    display: none;
  }
  }

</style>



## Absorption Calculator
<p class="desktop">If someone's broken this sheet, is currently editing, or you want the master sheet:&nbsp;<a href="https://docs.google.com/spreadsheets/d/1el_mW517XV3viFN6voXxQpg2PTrq4xuy65R4zEKbGr0/edit?usp=sharing" target="_blank"><t>click here</t></a>.</p>

<div class="desktop">
<iframe width="100%" height="100%" src="https://docs.google.com/spreadsheets/d/1dG5PGholXP_6kcKXk43Own0J5Q2LWktTknxIvmzkDc0/edit?usp=sharing?&amp;rm=minimal&amp;single=true&amp;headers=false&amp;"></iframe>
</div>
<p class="mobile">Unfortunately the calculator isn't usable from mobile/windows this small, <a href="https://docs.google.com/spreadsheets/d/1el_mW517XV3viFN6voXxQpg2PTrq4xuy65R4zEKbGr0/edit?usp=sharing" target="_blank"><t>please tap here to make a copy in Google Sheets</t></a>.</p>

---
