.TBG Unpacker
-------------

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
  TBGU is a small tool to unpack files which have been packaged in the .TBG format. Rather than requring loading of a program, and the use of commands in layers of menu's, TBGU allows the contained file to be quickly extracted to the current directory. Text associated with the contained file is not extracted, and is not added to the dialog.tlk file. Currently .tbg V4 files are supported, although its is likely the tool will be expanded to support the other .tbg formats.
This release fixes a bug relating to filenames with 8 characters.

+) Section 2. (un)Installation
==============================
To install TBGU simply unzip tbgu(xx).zip (where (xx) represents the version of TBGU). Popular unzipping tools include Winzip (http://www.winzip.com/) and Filzip (http://www.filzip.com/). Once the files are extracted you can place them wherever you like. Files included in the distribution are:
  readme.txt - this file
  tbgu.exe - the tbgu executable

To uninstall TBGU just delete the files you extracted from tbgu(xx).zip. The TBGU distribution includes no external dll files, and creates no registry entries.

+) Section 3. Usage
===================
TBGU runs as a console application, so there is not much of a GUI. The 2 ways of running TBGU are:
  i) Interactive (not included in this version)
    Just run (double-click) TBGU in Windows Explorer. TBGU will run interactivly, asking for the necessary information.

  ii) Command-line
    TBGU can be run from the command-line (shortcut, run dialog, DOS box, batch file). Usage in this mode is:
      TBGU input.tbg
      
    If no command-line parameters are specified, TBGU will run in interactive mode.
    
NB: Associated text is not extratced, and is not added to the dialog.tlk file. This means the any text used inthe item file will likely be incorrect. However, this also means you can quickly extract files without worrying about cluttering up the .tlk file, remebering to make backups, or remembering to remove files from the override directory. TBGU is meant as a quick extraction tool, so allow you to see how the files inside .tbg archives work, without requring full installation of the archive.
    
+) Section 4. Known Issues
==========================
If you find any errors, please let me know immediately, specifying as much as you can about your problem.

+) Section 5. Thanks to
=======================
This tool would not have taken a lot longer to produce without:
  + IESDP - http://www.teambg.com/iesdp

  + DLTCEP by Avenger was used to check resulting files.

+) Section 6. Contact Details
=============================
TBGU related e-mail should be sent to bg2@mcwrench.com
TBGU was programmed by bt_igi / igi (Marc Wrench)