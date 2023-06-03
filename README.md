The primary goal of this localization mod is to completely remove ambiguity from all vehicle names in all cases while at the same time keeping names as close to Gaijin's default names as possible. In most cases, the only name that has been changed is the one that appears at long range (>1.2km) which now matches the close and medium range name. The majority of the name changes are mostly minor syntax changes for the sake of consistency. Early and Late have been stylized as [E] and [L]. NATO names have been added to the statcards of aircraft that had them. Taiwanese vehicles have been given a sun icon. This mod works with any language selected, however the names of vehicles will always be in English. Yak-141 has been renamed to Yak-41M as this name is more accurate to the version we have in War Thunder.

The "new icons" version replaces the default roundel icon on French and Italian vehicles with alternative symbols. If you don't like the symbols I used, you can easily change them for all vehicles of a given nation at the same time by using the "replace all" tool in a software like Notepad++. The dechinafied version gives soviet names to chinese copy-paste vehicles. 

To save the units.csv file from github, open the folder of the version you want, click on units.csv, click "raw", right click → save as, and save the file somewhere convenient. Do not rename it. 

IMPORTANT NOTE: when using custom localization, your lang folder is frozen and no longer auto-updates. When Gaijin adds new texts, they will appear broken until you update the lang folder manually. Once you are familiar with the process of updating your lang folder it only takes about a minute to do. 

The version of the commit reflects the version of the game at the time I last updated the mod. I try to keep this repository as up to date as possible. If you need to nudge me to update it or if you have any other problems/concerns, feel free to reach out to me on discord: Jæk#5326

## Instructions

### To install

* Find your War Thunder files. The easiest way to do this is to look for aces.exe in task manager while the game is running, right click it and go to file location, and then go back one level to see your root files

* Open config.blk with any text editing software such as Notepad or Notepad++. Scroll down to the debug section. Add a new line `testLocalization:b=yes`, checking to make sure spelling and spacing are correct. It should look like this:
```
debug{
  enableNvHighlights:t="auto"
  screenshotAsJpeg:b=yes
  512mboughttobeenoughforanybody:b=yes
  testLocalization:b=yes
}
```
* Save the file
* Launch the game
* A new folder called "lang" should have appeared. Open the folder, inside should be multiple CSV files. Replace the default units.csv with the one you downloaded from this github
* Restart the game

### To update

* Go to your War Thunder files and delete the lang folder entirely
* Switch the language in the hangar to Russian (or restart the game)
* A new lang folder should have generated. Replace units.csv with the new one
* Switch the language back to English (or restart the game)

Switching languages is faster and more convenient than restarting. It also updates/fixes the hidden langRegional folder, so if you see broken texts for titles or challenges, cycling your language will usually fix it. 

### To Uninstall

*Delete the lang folder entirely
*Remove the `testLocalization:b=yes` line from config.blk