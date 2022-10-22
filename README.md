This repository contians the lang folder required to use War Thunder's custom localization system, which allows users to edit texts within the game such as vehicle names or kill messages. As of the Wind of Change update, the game no longer recompiles a missing lang folder if testlocalization is enabled; instead, the game crashes and throws Error 81110007 when it fails to find localization.blk. To continue using custom localization, I have started datamining the lang folder, and I am now uploading it here as a resource for those who need it. If the bug is fixed, this repositiroy will be discontinued.

The version name of the commit reflects the version of the War Thunder client (as shown on the launcher) that the lang folder was datamined from. When the dev server is open, version numbers will be even (if 2.19 is the live server, then 2.20 is the dev server) until the update is released; these dev server versions should work on the live server client without issue. 

I will try to keep this repository as up to date as possible. If you need to nudge me to update it or if you have any other problems, feel free to reach out to me on discord: Jæk#5326

## Instructions

There are two main folders on this repository, Vanilla and Modded. The Vanilla folder contains localization datamined straight from the game, as-is, without any changes to any of the files; use this if you're just looking for War Thunder's default lang folder. Modded contains my own localization mod which has slight tweaks to the names of certain vehicles; more info can be found in that folder. 
Within each version you'll find a lang folder and a zip file. The zip file allows you to easily download the complete lang folder. The unzipped folder contains the same files, which can be seen and saved individually for more advanced users.
