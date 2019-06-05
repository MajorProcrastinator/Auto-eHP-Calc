# Auto eHP Calc
If you haven't figured it out, this calculator is for finding out eHP calculations.

## Important Note For Google Sheets (and possibly other non-Excel spreadsheets)
* If you plan to use this sheet on google sheets, follow this guide: https://imgur.com/a/Mp1OoAj
  * This set of instructions are outdated, but if you find which cell the guide is pointing you to, follow steps, and input 'Background Tables'!G8:**G19** when it tells you to, then you'll be fine. I'll work on a new set of instructions when I have time (and seeing my procrastinating, that'll take some time. Sorry.)

## Calc Settings

![image](https://cdn.discordapp.com/attachments/391458004454604811/576657315705520128/unknown.png)

* The top row represents equipment. You can disable calculations for a certain equipment (i.e., if you don't have an Imp. Rudder, you can turn it off to see equipment relevant only to you)
* The next row represents what kind of input for a specific stat or skill. Setting it as automatic will input fields automatically. Setting it as manual... well, you get it. 
   * The last option in the row can override any manual/automatic option in the previous fields and set every field input (except Heal) as manual or automatic (the default option is "Mixed", where the "All" option will not override anything)
* The next row is where you can input manual stats, or "Manual Input". If you set a field input as manual in the above row, this is where you manually input stats.
* The "Automatic Input" section is where you set the level of the desired ship and the name of the ship. This will input fields set as automatic automatically.
   * To get a retrofitted ship's stats, append "Kai" to the end of the ship's name (i.e., Jintsuu Kai)
   * To get a Bulin or Purin for the calc, just type in "Bulin" or "Purin"
* The "Map Settings" section is kinda self-explanatory (not shown on the image above becuz I'm too lazy to update it).
   * The "Time" section is obvious. You can change time to mess with the Repair Toolkit's regen skill.
   * The "Level Advantage" section is where you input the level difference between your ship and the enemy. If you overlevel the enemy, the "Level Advantage" put in should be positive, and if the enemy has higher levels than your ships, then the value should be negative.
   * The "Danger Level" section is where you put in the Danger Level (also known as "Threat Level") in the calculator. If the map's danger level has not been reduced, the value inputted should be 0. If the map's danger level has been reduced 1 danger level, then the value should be one, and so on.
   * The "DNG LVL Status" section is where you note if the map is on safe-mode or not. It's quite self-explanatory.
* The "Enemy Stats" sections allow you to mess with enemy stats.
   * The Luck and Hit is kinda easy. They're just numbers. Scroll down if you want a link to some PvE values for enemies.
   * The "Hull Class" and "Shell Type" aren't as obvious. These allow you change what bullets are being fired at your ship (which adjusts the modifiers associated with them). The "General" modifiers are supposed to represent no modifiers (or a multiplicative modifier of 1).
* The last row shows what stats the eHP is being calculated with.

## Newbie Settings
* If you're a pure noob, just leave *everything* except the Ship Stats sections untouched. This should save you a lot of thinking. If you want to learn more about the other mechanics and details thrown into the calc., scroll through the [wiki](https://azurlane.koumakan.jp) (the Combat page is quite detailed if you're up for the flood of maths and formulas), or just hit up someone on the Official Azur Lane Discord (I'm open for PM's! Maybe.)

## Calculator
![image](https://cdn.discordapp.com/attachments/391458004454604811/576661952940736522/unknown.png)

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
