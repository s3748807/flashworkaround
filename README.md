Flash Workaround for Windows 10 using Mozilla Firefox v84.0.2 and Flash v32.0.0.314
================================

**Since Adobe no longer supports Flash Player after 31 December 2020 and blocked Flash content from running in Flash Player beginning 12 January 2021, Adobe strongly recommends all users immediately uninstall Flash Player to help protect their systems. The following workaround is unofficial and not associated with Adobe or Flash in any way.  I assume no responsibility or liability for any issues resulting from the implementation of this workaround. The information contained in this repo is provided on an "as is" basis with no guarantees of completeness, accuracy or functionality.

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

1. Fully uninstall any existing versions of Mozilla Firefox, including manually deleting any data that may be found in %USERPROFILE%\AppData\Local\Mozilla\Firefox
2. Uninstall Flash either manually or by running 'uninstall_flash_player.exe' provided by Adobe which has been provided for use in the 'files' directory of this repo.
3. Reinstall Mozilla Firefox by running 

Contact
=======


**Michael McAlary** - s3748807@student.rmit.edu.au

**Project Link** - https://github.com/s3748807/CPT264assignment2
