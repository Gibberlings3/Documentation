Scroll Creator for the Infinity Engine
--------------------------------------

+) Contents
===========
1.    About
2.    (Un)Installation
3.    Usage
4.    Known Issues
5.    Thanks to
6.    Contact Details

+) Section 1. About
===================
  Scroll Creator for the Infinity Engine (SCCIE) is a small tool to aid in the creation of .itm files for Infinity Engine games, specifically scrolls used to learn/cast magic spells. Currently BG1, BG1:ToSc, BGII:SoA, BGII:ToB, IWD1 (and add-ons) are supported (ie. games using ITM/SPL V1 files), although its is likely the tool will be expanded to support the other IE games.

+) Section 2. (un)Installation
==============================
To install SCCIE simply unzip sccie(xx).zip (where (xx) represents the version of SCCIE). Popular unzipping tools include Winzip (http://www.winzip.com/) and Filzip (http://www.filzip.com/). Once the files are extracted you can place them wherever you like. Files included in the distribution are:
  readme.txt - this file
  sccie.exe - the sccie executable

To uninstall SCCIE just delete the files you extracted from sccie(xx).zip. The SCCIE distribution includes no external dll files, and creates no registry entries.

+) Section 3. Usage
===================
SCCIE runs as a console application, so there is not much of a GUI. The 2 ways of running SCCIE are:
  i) Interactive (not included in this version)
    Just run (double-click) SCCIE in Windows Explorer. SCCIE will run interactivly, asking for the necessary information.

  ii) Command-line
    SCCIE can be run from the command-line (shortcut, run dialog, DOS box, batch file). Usage in this mode is:
      SCCIE input.spl output.itm
      
    If no command-line parameters are specified, SCCIE will run in interactive mode.
    
SCCIE will read in the .spl file, and create a .itm file scroll, with the correct usability restriction, use-icon, and abilities (cast the spell, and learn the spell). The icon assigned to the spell is assigned using the standard IE naming scheme, of filenameA (with filenameB and filenameC being used for spellbook and memorisation icons). The range and target type information are read from the 1st extended header in the .spl file, so the extended headers should be arranged so as the level 1 extension header comes 1st.
    
+) Section 4. Known Issues
==========================
  Usability restrictions do not take into account the spell exclusion school.

If you find any errors, please let me know immediately, specifying as much as you can about your problem.

+) Section 5. Thanks to
=======================
This tool would not have taken a lot longer to produce without:
  + IESDP - http://www.teambg.com/iesdp

  + DLTCEP by Avenger was used to check resulting files.

+) Section 6. Contact Details
=============================
SCCIE related e-mail should be sent to bg2@mcwrench.com
SCCIE was programmed by bt_igi / igi (Marc Wrench)