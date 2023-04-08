The goal of this localization mod is to completely remove ambiguity from vehicle names while keeping them as close to default as possible. In most cases, the only name that has been changed is the one that appears at long range (>1.2km) which now matches the close and medium range name. The few that have been renamed are mostly minor syntax changes for the sake of consistency. Early and Late have been stylized as [E] and [L]. NATO names have been added to the statcards of eastern planes. Taiwanese vehicles have been given a sun icon. The "new icons" version replaces the default roundel icon on French and Italian vehicles with alternative symbols. The "dechinafied" version has Soviet names for copy-pasted Chinese vehicles. This mod works with any language selected, however the names of vehicles will always be in English.

To save the units.csv file from github, open the folder of the version you want, click on units.csv, click "raw", right click → save as, and save the file somewhere convenient. Do not rename it. 

IMPORTANT NOTE: when using custom localization, your lang folder is frozen and no longer auto-updates. If you start seeing broken texts, particularly when a major update is released, you will need to manually update your lang folder, which is quick process once you learn how to do it. 

The version of the commit reflects the version of the game at the time I last updated the mod. I try to keep this repository as up to date as possible. If you need to nudge me to update it or if you have any other problems/concerns, feel free to reach out to me on discord: Jæk#5326

## Instructions

###To install

•Find your War Thunder files. The easiest way to do this is to look for aces.exe in task manager while the game is running, right click it and go to file location, and then go back one folder to see your root files
•Open config.blk with any text editing software such as Notepad or Notepad++. Scroll down to the debug section. Add a new line `testLocalization:b=yes`, checking to make sure spelling and spacing are correct. It should look like this:
```
debug{
  enableNvHighlights:t="auto"
  screenshotAsJpeg:b=yes
  512mboughttobeenoughforanybody:b=yes
  testLocalization:b=yes
}
```
•Save the file
•Launch the game
•A new folder called "lang" should have appeared. Open it and replace the default units.csv with the one you downloaded
•Restart the game

### To update

•Go to your War Thunder files, and delete the lang folder entirely
•Switch the language in the hangar to Russian (or restart the game)
•A new lang folder should have generated. Replace units.csv with the new one
•Switch the language back to English (or restart the game)

Switching languages is faster and more convenient than restarting. It also updates/fixes the langRegional folder, so if you see broken texts for titles or challenges, cycling your language will usually fix it. 

### To Uninstall

•Delete the lang folder entirely
•Remove the `testLocalization:b=yes` line from config.blk