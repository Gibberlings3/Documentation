======================================
G3 Mod Packaging Made Easy
Brought to you by Mike1072 and CamDawg
======================================

This utility is designed to package up versions of your mod for all operating systems to match standard G3 conventions. 

The archive includes Real Mod, a fully-functioning mod that showcases how to use this packaging utility and serves as
an example of current best practices to deal with audio conversion, character set handling, and tileset decompression.


======================
Packaging Instructions
======================

1)
    Put your mod in this folder.  You don't need to worry about including WeiDU or .command files; these will be created for you.

2)
    Make sure your icons are up to date.  Replace yours with the latest ones from the real_mod\style directory.

3)
    Make sure the Mac programs your mod uses are up to date.  If you use audio, grab the latest sox from the real_mod\audio directory.
    If you use tilesets, grab the latest tisunpack from the real_mod\tiz\osx directory.
   
4)
    Create a copy of package_real_mod.bat and call it package_your_mod.bat or whatever you like.
   
5)
    Use a text editor to modify package_your_mod.bat so the information reflects the particulars of your mod.
   
6)
    Run package_your_mod.bat to automatically package your mod for all operating systems.

7)
    When you update your mod later and want to release a new version, just update your mod files in this folder and repeat steps 5 and 6.


===================
Contact Information
===================

Comments about this utility can be directed to this forum thread:

http://www.gibberlings3.net/forums/index.php?showtopic=26717


===============
Version History
===============

Version 4 - March 7, 2015

    - Updated to WeiDU v238
    - Added option to prevent lowercasing filenames
    - Fixed archive creation when .tp2 is outside of mod folder


Version 3 - February 15, 2015

    - Replaced fnr with sed to improve compatibility under Wine, thanks to AstroBryGuy


Version 2 - January 6, 2015

    - Updated to WeiDU v237
    - Replaced OS X version of tisunpack with a more compatible one provided by StefanO


Version 1 - October 3, 2014

    - Initial release packaged with WeiDU v236
