# Auto eHP Calc
If you haven't figured it out, this calculator is for finding out eHP calculations.

### Yeah, I know that this documentation is screwed up. I'll update it later. Probably.

## Important Note For Google Sheets (and possibly other non-Excel spreadsheets)
* If you plan to use this sheet on google sheets, follow this guide: https://imgur.com/a/Mp1OoAj
  * This set of instructions are outdated, but if you find which cell the guide is pointing you to, follow steps, and input 'Background Tables'!G8:**G19** when it tells you to, then you'll be fine. I'll work on a new set of instructions when I have time (and seeing my procrastinating, that'll take some time. Sorry.)

## Calc Settings (Section in need of an update. Figure it out by yourself for now)

![image](https://cdn.discordapp.com/attachments/391458004454604811/576657315705520128/unknown.png)

* The top row represents equipment. You can disable calculations for a certain equipment (i.e., if you don't have an Imp. Rudder, you can turn it off to see equipment relevant only to you)
* The next row represents what kind of input for a specific stat or skill. Setting it as automatic will input fields automatically. Setting it as manual... well, you get it. 
   * The last option in the row can override any manual/automatic option in the previous fields and set every field input (except Heal) as manual or automatic (the default option is "Mixed", where the "All" option will not override anything)
* The next row is where you can input manual stats, or "Manual Input". If you set a field input as manual in the above row, this is where you manually input stats.
* The "Automatic Input" section is where you set the level of the desired ship and the name of the ship. This will input fields set as automatic automatically.
   * To get a retrofitted ship's stats, append "Kai" to the end of the ship's name (i.e., Jintsuu Kai)
   * To get a Bulin or Purin for the calc, just type in "Bulin" or "Purin"
* The "Map Settings" section (not shown on the image above becuz I'm too lazy to update it) is where you put in values related to the map and the enemies on it.
   * The "Time" section is obvious. You can change time to mess with the Repair Toolkit's regen skill.
   * The "Level Advantage" section is where you input the level difference between your ship and the enemy. If you overlevel the enemy, the "Level Advantage" put in should be positive, and if the enemy has higher levels than your ships, then the value should be negative.
   * The "Danger Level" section is where you put in the Danger Level (also known as "Threat Level") in the calculator. If the map's danger level has not been reduced, the value inputted should be 0. If the map's danger level has been reduced 1 danger level, then the value should be one, and so on.
   * The "DNG LVL Status" section is where you note if the map is on safe-mode or not. It's quite self-explanatory.
   * The "Fire" section is where you would turn on an estimation of fire. As for how much estimation is going on, scroll on down!
* The "Enemy Stats" sections allow you to mess with enemy stats.
   * The Luck and Hit is kinda easy. They're just numbers. Scroll down if you want a link to some PvE values for enemies.
   * The "Hull Class" and "Shell Type" aren't as obvious. These allow you change what bullets are being fired at your ship (which adjusts the modifiers associated with them). The "General" modifiers are supposed to represent no modifiers (or a multiplicative modifier of 1).
* The last row shows what stats the eHP is being calculated with.

### Notes on Fire

**Right now, Fire is kinda janky. I forgot to account for misses, so fire dmg seems to be artificially high**

This is an **estimation**. Fire is weird. It doesn't stack, it has a duration, and the formula has a constant in it. The first estimation comes from the fact I had to ignore the constant (and a bunch of other variables that my calculator doesn't need). if I wanted my eHP Calculator to include fire. The next few require some more explanation. In creating a fire modifier for my eHP calc, I broke it down to 5 parts: FireProbabilityPerBullet (a percent), BulletsFiredPerVolley (not a percent), FireDuration (not a percent), ReloadDuration (not a percent), DamageModifier (percent). The formula for the modifier came out like this:

![image](https://cdn.discordapp.com/attachments/391458004454604811/593565575096041482/unknown.png)

* FireProbabilityPerBullet is simple; it's straight from the wiki. This is accurate.
* BulletsFiredPerVolley is an integer value I chose based on how many shells the BiS guns of each hull class fires and my estimation of how frequently a gun is used given multiple BiS guns. "PerVolley" is also an inaccurate description. Since some ships (i.e., battleships), have more than one Main Gun Mount, I had to take in account that. Hence BB guns that might fire 3 or 2 shells, will be noted as firing many more than that. CL and CA guns will see similar scalings. This is prone to inaccuracy.
* ReloadDuration is based off a similar way of estimation, except instead of bullet count, reload time is used. This estimation is also muddled further by my estimation of how much reload stat affects reload time and by my rounding to the nearest whole or half of a number. Also, like how BulletsFiredPerVolley had Main Gun Mount estimations, the ReloadDuration skips factoring in the slight delay between volleys. This one is seriously prone to inaccuracy.
* FireDuration is a set value given from the wiki: 15 seconds. However, it can be affected by skills and equipment. This is also accurate.
* DamageModifier is usually 1. However, this can also be affected by skills and equipment. This is also accurate.

Regardless, since this calculator is really more of a reference when it comes to eHP, this Fire Modifier estimation could probably be forgiven. In the future, I might consider making fire modifier that allows custom reload times and bullets fired to insure better accuracy. However, given the already complicated nature of my calculator, I decided against it for now.

## Newbie Settings
* If you're a pure noob, just leave *everything* except the Ship Stats sections untouched. This should save you a lot of thinking. If you want to learn more about the other mechanics and details thrown into the calc., scroll through the [wiki](https://azurlane.koumakan.jp) (the Combat page is quite detailed if you're up for the flood of maths and formulas), or just hit up someone on the Official Azur Lane Discord (I'm open for PM's! Maybe.)

## Calculator
![image](https://cdn.discordapp.com/attachments/391458004454604811/593565575096041482/unknown.png)

* Uh... There's not much to say...
* Green represents better eHP; red is worse.
* This was quite obvious, wasn't it?

## Legacy
* This is the old calculator. Use if you're having issues with the new one.

## Other
* No more equipment meme names, unless you want to go looking through the innards of the calculator for them. Memeworthiness not guaranteed.
* Enemy Hit stat can vary, however, most people like to use 45 or 50
* Enemy Luck stat can also vary, but for PvE, most of the time, it's 0.
* You can find out exact enemy stats here: https://al-data.github.io/enemies
* Formation Bonuses have not been applied, but you can throw them into manual input (Evasion Stat Buff).
    * Single Line: -.1
    * Double Line: .3
    * Diamond: 0
* If you want to see the background workings of the calculator, you have to unhide those sheets. You can change the values on the Ship Stats sheet with minimal impact, but the Background Tables sheet is different. Don't mess with that one.
* If you're github illiterate, just click on the Automatic eHP Calc.xlsx file and hit download at the top right. That's not too hard, right? Or am I having too high hopes for humanity?


If I am having too high hopes for humanity, send a message to Maj. Procrastinator#8734 or contact me on the Azur Lane Official Discord #help channel. (Or just hit me up for questions about the calculator. I'm mostly humane in my treatment of new #help victims)

(Btw, Warspite is a Corgi)
