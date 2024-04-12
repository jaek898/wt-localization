The primary goal of this localisation mod is to completely remove ambiguity from all vehicle names in all cases while at the same time keeping names as close to Gaijin's default names as possible. In most cases, the only name that has been changed is the one that appears at long range (>1.2km) which now matches the close and medium range name. The majority of the name changes are mostly minor syntax changes for the sake of consistency. Early and Late have been stylized as [E] and [L]. NATO names have been added to the stat cards of aircraft that had them. Taiwanese vehicles have been given a sun icon. This mod works with any language selected, however the names of vehicles will always be in English. Yak-141 has been renamed to Yak-41M as this name is more accurate to the version we have in War Thunder.

The Standard version uses default French/Italian roundels. The New Icons version replaces the default roundel icon on French and Italian vehicles with alternative symbols. If you don't like the symbols I used, you can easily change them for all vehicles of a given nation at the same time by using the "replace all" tool in software like Notepad++. The Dechinafied version, requested by [General Lee](https://www.youtube.com/@GeneralLee2000), gives Soviet names to Chinese copy-paste vehicles in addition to the new French/Italian roundels.

The easiest way to save the contents from GitHub is to use the "copy raw contents" button, which saves the contents of the entire file to your clipboard. If this method does not work you can view the raw files, right-click, and use "save as" to save them wherever you want. 

IMPORTANT NOTE: when using custom localisation, your lang folder is frozen and no longer auto-updates. When Gaijin adds new texts, they will appear broken until you update the lang folder manually. Once you are familiar with the process of updating your lang folder it only takes about a minute to do. 

The version of the commit reflects the version of the game at the time I last updated the mod. I try to keep this repository as up-to-date as possible. If you need to nudge me to update it or if you have any other problems/concerns, feel free to reach out to me  with a DM on discord: Jæk#5326

# Instructions

## To install

[Video example](https://youtu.be/KknlZ8sc3xA)

- Open your War Thunder files

  - *If you don't know where your files are located, the easiest way to find them is to run the launcher, and then use "open file location" in Task Manager.

- Open config.blk with any text editing software such as Notepad or Notepad++. Scroll down to the debug section. Add a new line `  testlocalisation:b=yes`, checking to make sure spelling and spacing are correct. It should look like this:
```
debug{
  screenshotAsJpeg:b=yes
  512mboughttobeenoughforanybody:b=no
  enableNvHighlights:t="auto"
  testlocalisation:b=yes
}
```
- Save the file
- Launch the game
- A new folder called "lang" should have appeared. Open the folder, inside it, there should be multiple CSV files.
- units.csv is the file responsible for vehicle names. Your goal is to replace the default units.csv with the custom one from this GitHub.
  - The easiest way to do this is to use the "Copy raw contents" button as described in the third paragraph. Open units.csv with a text editor like Notepad or Notepad++, use ctrl+A to select all, delete everything, and then paste in what you just copied. If it is pasted successfully, save the file and close it. 
  - If for whatever reason that method didn't work, try using the other method where you save the units.csv file from GitHub. Drag it into your lang folder. Choose to replace if prompted. 
- Restart the game OR switch your language in the hangar to Russian and back to English

## To update

[Video example](https://youtu.be/0tRrfIAt1o8)

When you start seeing broken texts, you will need to update your lang folder manually. This is particularly important when Gaijin releases a major update as major updates bring numerous new vehicle and menu texts. 
- With the game running, go to your War Thunder files and delete the lang folder entirely
- In the hangar, go to options, and change your language to Russian. Apply the setting and make sure your language changes. Hit esc if a popup comes up prompting you to download additional content.
- A fresh lang folder should have been generated. Refresh File Explorer if you do not see it. Replace the contents of units.csv as you have done before. 
- Tab back into War Thunder and switch the language back to English (or whatever language you were using). 

Switching languages is faster and more convenient than restarting the game. It also updates/fixes the hidden langRegional folder, so if you see broken texts for titles or challenges, cycling your language will usually fix it. 

## To Uninstall

- Delete the lang folder entirely
- Remove the `testlocalisation:b=yes` line from config.blk

### Troubleshooting

> Vehicle names are broken and show up as codes (for example, mig-17p_lim_5p instead of Lim-5P)

If this only appears on recently added vehicles, update your localisation.
If this happens to all vehicles, the game is not reading units.csv correctly. Make sure units.csv is in the lang folder, that there is only one, and the contents look correct.

> Vehicle names are loading properly, but the national symbols are not

War Thunder uses some interesting Unicode characters which it "converts" to the national symbols you see in-game. If these symbols are not loading correctly, likely, that the file did not save correctly from GitHub. Try saving the contents using a different method. 

> Lang folder is not appearing

Check to make sure you put `testlocalisation:b=yes` in the correct section, spacing and formatting are correct, you saved the file, you restarted the game, and you're looking in the right directory.

> Text for titles or challenges is broken

Cycle to any other language (make sure the language in the hangar properly changes) and then back to the language you were using. 
