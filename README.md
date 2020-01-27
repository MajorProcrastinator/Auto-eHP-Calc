## Note
Check out [Enbayft's](https://github.com/Enbayft/Random-AL-Stuff) DPS eHP calc. Since I've been noticeably lazy with updating my calc, I decided to implement my eHP calc into Enbayft's DPS calc, considering his much more regular updates on the thing. 

**Loss of Features**
* Lv. 100 stats (Lost much relevance in after EN received Lv. 120)
* Automatic Skill Input (I don't think I would've got to this anyways)

**New Features**
* VH Armor Plating

## Calc Settings

![image](https://cdn.discordapp.com/attachments/391458004454604811/603000555219976193/unknown.png)

* **Equipment Settings -** You can disable calculations for a certain equipment (i.e., if you don't have an Imp. Rudder, you can turn it off to see equipment relevant only to you)
* **Ship Stat Input Settings -** You can choose what kind of input you want for a specific stat or skill. Setting it as automatic will input fields automatically. Setting it as manual... well, you get it. 
   * The "All" can override any manual/automatic option in the previous fields and set every field input as manual or automatic (the default option is "Mixed", where the "All" option will not override anything)
* **Manual Input -** If you set a field input as manual in the above row, this is where you manually input stats.
* **Automatic Input -** This section is where you set the level of the desired ship and the name of the ship. This will input fields set as automatic automatically.
   * To get a retrofitted ship's stats, append "Kai" to the end of the ship's name (i.e., Jintsuu Kai)
   * To get a Bulin or Purin for the calc, just type in "Bulin" or "Purin"
* **Enemy Stats -** This section is where you mess with stats and classications related to the attacking enemy.
   * The Luck and Hit is kinda easy. They're just numbers. Scroll down if you want a link to some PvE values for enemies.
   * The "Hull Class" and "Shell Type" aren't as obvious. These allow you change what bullets are being fired at your ship (which adjusts the modifiers associated with them). The "General" modifiers are supposed to represent no modifiers (or a multiplicative modifier of 1).
* **Map Settings -** This section is where you put in values related to the map and the enemies on it.
   * The "Time" option is obvious. You can change time to mess with the Repair Toolkit's regen skill.
   * The "Level Advantage" option is where you input the level difference between your ship and the enemy. If you overlevel the enemy, the "Level Advantage" put in should be positive, and if the enemy has higher levels than your ships, then the value should be negative.
   * The "Danger Level" option is where you put in the Danger Level (also known as "Threat Level") in the calculator. If the map's danger level has not been reduced, the value inputted should be 0. If the map's danger level has been reduced 1 danger level, then the value should be one, and so on.
   * The "DNG LVL Status" section is where you note if the map is on safe-mode or not. It's quite self-explanatory.
* **Fire Settings -** This section is where you control stuff related to fire.
   * The "Fire" option is where you choose if you want fire on or off.
   * The "Gun Fire Rate" input is *absolutely necessary* if you want fire to calculate properly. This is the enemy's fire rate.
   * The "Shells on Target" input is *absolutely necessary* for fire calculations. This is how where you input how many of the enemy shells hit your ships in one reload cycle (i.e., Duke of York releases an artillery strike and only 6 shells physically land on the target. You would enter 6 in this example)

### Notes on Fire

This is an **estimation**. Fire is weird. It doesn't stack, it has a duration, and the formula has a constant in it. The first estimation comes from the fact I had to ignore the constant (and a bunch of other variables that my calculator doesn't need). if I wanted my eHP Calculator to include fire. The next few require some more explanation. In creating a fire modifier for my eHP calc, I broke it down to 5 parts: FireProbabilityPerBullet (a percent), BulletsFiredPerVolley (not a percent), FireDuration (not a percent), ReloadDuration (not a percent), DamageModifier (percent). The formula for the modifier came out like this:

![image](https://cdn.discordapp.com/attachments/391458004454604811/593565575096041482/unknown.png)
(Note, the ReloadDuration and FireDuration are actually switched)

* FireProbabilityPerBullet is simple; it's straight from the wiki. This is accurate.
* BulletsFiredPerVolley is "Shells on Target" in Fire Settings.
* ReloadDuration is the "Gun Fire Rate" in Fire Settings.
* FireDuration is a set value given from the wiki: 15 seconds. However, it can be affected by skills and equipment. This is also accurate.
* DamageModifier is usually 1. However, this can also be affected by skills and equipment. This is also accurate.

## Newbie Settings
* If you're a pure noob, just leave *everything* except the Ship Stats sections untouched. This should save you a lot of thinking. If you want to learn more about the other mechanics and details thrown into the calc., scroll through the [wiki](https://azurlane.koumakan.jp) (the Combat page is quite detailed if you're up for the flood of maths and formulas), or just hit up someone on the Official Azur Lane Discord (I'm open for PM's! Maybe.)

## Calculator
![image](https://cdn.discordapp.com/attachments/391458004454604811/602998321526865926/unknown.png)

* The top section is where the calculator pull numbers and stuff to calculate values.
* Uh... There's not much to say...
* Green represents better eHP; red is worse.

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
