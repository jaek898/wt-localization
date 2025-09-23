The primary goal of this localization mod is to address minor inconsistencies in Gaijin's default vehicle names, not to overhaul names for historical accuracy. In general, I try to leave vehicle names as close to default as possible for the sake of recognition and familiarity. The most common changes I've made are applying more consistent syntax rules, such as stylizing Early and Late as `[E]` and `[L]`, relegating block number to the statcard in cases where it is not relevant, applying national symbols where needed to differentiate vehicles, and applying consistent formatting to British postwar aircraft (e.g., by default, Gaijin uses `FAW 20`, `F.(A.W.) Mk 9`, and `F.A.W. Mk.2`; these are changed to `FAW.20`, `FAW.9`, and `FAW.2` respectively). Israeli aircraft have had their names reverted to using their American names with a national symbol, when applicable (Netz becomes `✡A-4N`, Baz becomes `✡F-15A`, etc.). `Yak-141` has been renamed to `Yak-41M`. Supplemental information has been added in `[brackets]` when required for differentiation; for example, multi-piece SAM systems use `[TEL]` or `[TADS]` to differentiate their launch vehicles from their target acquisition vehicles. NATO reporting names have been added to statcards for eastern vehicles, when applicable. All vehicles use the same names across all ranges; this means detail does not "pop-in" as you get closer to an enemy vehicle. This is done for the sake of consistency and is permitted, according to Stona. This lang mod works regardless of which language you use in the game.

National symbols are generally used to differentiate vehicles from their origin countries. I have changed the symbol for Taiwanese vehicles to use a sun icon (`☀`) that resembles the national flag (by default, Gaijin uses the PRC stars icon across all Chinese vehicles). By default, Gaijin uses the same concentric circles roundel for British, French, Italian, Thai, Belgian, Finnish, and Iranian vehicles. To combat this, I have made of a version which replaces the French and Italian roundels with alternative symbols. If you don't like the symbols I used, you can easily replace them by using "replace all" in Notepad++ or a similar tool. You can test if a symbol will work in vehicle names by pasting it into any text box in the game. I'm always looking for new unicode characters to use as roundels, in particular for Thai vehicles, but have not found any suitable alternatives yet.

This mod **ONLY** affects unit names. It does not affect weapon names, UI text, RWR threats, kill messages, or anything else pertaining to the lang folder. In other words, changing the units.csv text can only affect the names of vehicles that you can play or vehicles/targets you can destroy for RP.

To save the contents of the file from github, click on the folder of the version you want, click on units.csv, and then click "copy raw file". If this does not work for you, click "raw", then right click and select "Save as..."

IMPORTANT NOTE: when using custom localization, your entire lang folder is frozen and no longer auto-updates! Gaijin seems to have changed the way the lang folder handles texts that are missing from the files. Instead of appearing as a string of internal text, it autofills them with localizaed text from the default folder. You will still have to at minimum update your units.csv file with a new version from this github if you want the changes I've made to apply to newly added vehicles. Updating your lang folder with a new version of this mod takes less than a minute to do once you become proficient at it.

When using custom localization, the hidden regional lang folder may break, which causes text such as titles or monthly challenges to appear broken. To fix this, simpily switch language in the hangar to Russian, make sure the change applied, and then switch back to whichever language you were using before.

The version of the commit on GitHub reflects the version of the game I most recently updated the file to. I try to keep this repo as up to date as possible. I usually add new vehicles soon after they hit the dev server, meaning the file is usually updated before vehicles even become obtainable (and you can use this mod on your dev server client if you want). If you need to nudge me to update something or if you have any other problems/feedback/concerns, the best way to reach out to me is by pinging me in the #localization-discussion channel in my [Discord server](https://discord.com/invite/gd48uehmsU). I also post the changelog there. 

# Instructions

## Enable custom localization
- Open the options in the hangar. In the "Main parameters" tab, enable the "Custom localization" option. Restart the game when prompted.

  - You should now see the warning text "Custom localization enabled" in the top left of the hangar, beneath the player count. If you do, continue to installation
<details>
<summary>Alternative (old) method for enabling custom localization</summary>

  
  [Video example](https://youtu.be/KknlZ8sc3xA)

Use this method if the method above did not work for you. 

- Open your War Thunder files

  - *If you don't know where your files are located, the easiest way to find them is to run the launcher, then use "open file location" in task manager*

- Open config.blk with any text editing software such as Notepad or Notepad++. Scroll down to the debug section. Add a new line `testLocalization:b=yes`, checking to make sure spelling and spacing are correct. It should look like this:
```
debug{
  enableNvHighlights:t="auto"
  screenshotAsJpeg:b=yes
  512mboughttobeenoughforanybody:b=yes
  testLocalization:b=yes
}
```
- Save the file
- Launch the game
</details>

## Installation
- You should see the warning text "Custom localization enabled" in the top left of the hangar, beneath the player count. A new folder called "lang" should have appeared. It should contain numerous CSV files.
- units.csv is the file responsible for vehicle names. Your goal is to replace the default units.csv with the custom one from this GitHub.
  - The easiest way to do this is to use the "Copy raw contents" button as described in the third paragraph. Open units.csv with a text editor like notepad or notepad++, use ctrl+A to select all, delete everything, then paste in what you just copied. If it pasted successfully, save the file and close it. 
  - If for whatever reason that method doesn't work for you, try opening the raw file, right clicking, and selecting "Save as...". Drag it into your lang folder. Replace if prompted. 
- Restart the game OR switch your language in the hangar to Russian and back to English

## Updating

You will need to update the units.csv file if you want the changes I've made to apply to newly added vehicles. This can be done by replacing the contents of the units.csv file with the new version, just as you did when initially installing, and then cycling languages or restarting the game to refresh localization and apply the changes. If you see broken texts, you may need to generate a fresh lang folder.

<details>
<summary>Lang folder regeneration</summary>

[Video example](https://youtu.be/0tRrfIAt1o8)

Previously, when Gaijin added new vehicles or text to the game, they would appear broken for custom localization users until they were manually added to the csv files. This meant it was necessary to regenerate the lang folder. If for whatever reason you still run into this issue, try regenerating the lang folder and then updating the contents of the units.csv file:

- With the game running, go to your War Thunder files and delete the lang folder entirely
- In the hangar, go to options, and change your language to Russian. Apply the change and make sure your language actually switches. Hit Esc if a popup comes up prompting you to download additional content.
- A fresh lang folder should have generated. Refresh file explorer if you do not see it. Replace the contents of units.csv with the new version from this github, just as you did when initially installing. 
- Tab back into War Thunder and switch the language back to English (or whatever language you were using before). 

Switching languages is faster and more convenient than restarting the game. As previously mentioned, it is also sometimes the only way to refresh the hidden regional lang folder.

</details>

## To Uninstall

- Disable the "custom localization" option in the hangar.
  - If that does not work, close the game, delete the lang folder entirely, and then remove the testLocalization:b=yes line from config.blk. Save the file and launch the game.

# Troubleshooting

> Vehicle names are broken and show up as codes (for example, mig-17p_lim_5p instead of Lim-5P)

If this only appears on recently added vehicles, update your units.csv with a new version.
If this happens to all vehicles, the game may not be reading units.csv correctly. Make sure units.csv is in the lang folder, that there is only one, and the contents look correct. Syntax errors somewhere in the units.csv file can cause it to break, such as improper use of quotation marks or semicolons. 

> Vehicle names are loading properly, but the national symbols are not

War Thunder uses some interesting unicode characters which it "converts" to some of the national symbols you see in game. If these symbols are not loading correctly, it is likely that the file did not save correctly from GitHub. Try saving the contents using a different method. 

> Lang folder is not appearing

Check to make sure you put `testLocalization:b=yes` in the correct section, syntax and spelling are correct, you saved the config file, you restarted the game, and you're looking in the correct directory.

> Text for titles or challenges is broken

Cycle to any other language (make sure the language in the hangar actually changes) and then back to the language you were using. 
