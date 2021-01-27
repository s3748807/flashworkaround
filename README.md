Flash Workaround for Windows 10 using Mozilla Firefox v84.0.2 and Flash v32.0.0.314
================================

**Since Adobe no longer supports Flash Player after 31 December 2020 and blocked Flash content from running in Flash Player beginning 12 January 2021, Adobe strongly recommends all users immediately uninstall Flash Player to help protect their systems. The following workaround is unofficial and not associated with Adobe or Flash in any way.  I assume no responsibility or liability for any issues resulting from the implementation of this workaround. The information contained in this repo is provided on an "as is" basis with no guarantees of completeness, accuracy or functionality.**

This repo provides a temporary workaround for continued use of Flash using Mozilla Firefox v84.0.2 and Flash v32.0.0.314, tested on Microsoft Windows 10 Education OS version 10.0.18362 Build 18362.  

Installation of Windows update 'KB4577586 - Adobe Flash Removal Update for Windows' will most likely prevent this solution from working, so ensure that this has not been applied to your system. Once applied, this update cannot be uninstalled. More information regarding the update can be found at https://support.microsoft.com/en-us/topic/update-for-the-removal-of-adobe-flash-player-october-27-2020-931521b9-075a-ce54-b9af-ff3d5da047d5 

Synopsis
========

This is a workaround that provides instructions to completely uninstall existings versions of Flash and Mozilla Firefox on Windows 10 before reinstalling an archived version of Flash and Firefox that are provided in this repo.  

Prerequisites
-------------


Before following the instructions ensure that  Windows update 'KB4577586 - Adobe Flash Removal Update for Windows' has not been applied. 

Additionally, ensure that if your enterprise environment is managing your computer build and Mozilla Firefox deployment that there are no policy settings that would override the configuration outlined in the installation steps.

This workaround has only been tested on a PC running Microsoft Windows 10 Education OS version 10.0.18362 Build 18362.  

Installation
------------

1. Fully uninstall any existing versions of Mozilla Firefox, including manually deleting any data that may be found in **%USERPROFILE%\AppData\Local\Mozilla\Firefox**
2. Reinstall Mozilla Firefox by running **'firefox_installer.exe'** which has been provided for use in the 'files' container of this repo.
3. Uninstall Flash by running **'uninstall_flash_player.exe'** which has been provided for use in the 'files' container of this repo.
4. Download and unzip **'fp_32.0.0.314_archive.zip'** which has been provided for use in the 'files' container of this repo.
5. Install the archived copy of Flash v32.0.0.314 NPAPI (for Mozilla Firefox) by running **'fp_32.0.0.314_archive.zip\32_0_r0_314\flashplayer32_0r0_314_winpep.msi'**
6. Disable all automatic updates within Mozilla Firefox and installed applications. This can be done by typing about:config into the url bar of Firefox and searching for autoupdate and changing the boolean to false.  There are also update settings under 'Options > Firefox Updates' that should all be disabled, including unchecking the 'Use a background service to install updates' option.
7. (Optional) Create a folder in the Mozilla root install directory called distribution (i.e. 'C:\Program Files\Legacy Mozilla Firefox\distribution') and create a json file called policies.json.  Within this .json file you are able to set policies that will be applied to the instance of Firefox when launched.  I have created a file which disables all auto updates and limits the domains that can be visited by Firefox to exclusively those needed for flash within my organisation.  A copy of this json file has been provided as an example in the 'files' container of this repo, however you will need to modify the domains listed under "WebsiteFilter" or you will not be able to browse to any other domain.

Contact
=======


**Project Link** - https://github.com/s3748807/flashworkaround
