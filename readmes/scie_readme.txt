Store Creator for the Infinity Engine
-------------------------------------

+) Contents
===========
1.    About
2.    (Un)Installation
3.    Usage
4.    Definition Files
5.    Known Issues
6.    Thanks to
7.    Contact Details

+) Section 1. About
===================
  Store Creator for the Infinity Engine (SCIE - pronounced sky) is a small tool to aid in the creation of .sto files for Infinity Engine games. Currently only BG1, BG1:ToSc, BGII:SoA and BGII:ToB are supported (ie. games using STO V1 files), although its is likely the tool will be expanded to support the other IE games.

+) Section 2. (un)Installation
==============================
To install SCIE simply unzip scie(xx).zip (where (xx) represents the version of SCIE). Popular unzipping tools include Winzip (http://www.winzip.com/) and Filzip (http://www.filzip.com/). Once the files are extracted you can place them wherever you like. Files included in the distribution are:
  input.txt - sample Definition File
  keywords.txt - list of keywords
  readme.txt - this file
  scie.exe - the scie executable

To uninstall SCIE just delete the files you extracted from scie(xx).zip. The SCIE distribution includes no external dll files, and creates no registry entries.

+) Section 3. Usage
===================
SCIE runs as a console application, so there is not much of a GUI. The 2 ways of running SCIE are:
  i) Interactive (not included in this version)
    Just run (double-click) SCIE in Windows Explorer. SCIE will run interactivly, asking for the necessary information.

  ii) Command-line
    SCIE can be run from the command-line (shortcut, run dialog, DOS box, batch file). Usage in this mode is:
      SCIE [compile | decompile] input.ext output.ext
      
    If no command-line parameters are specified, SCIE will run in interactive mode.
    
The two functions of SCIE are:
  a) Decompiling
    Using this funtion you can quickly decompile an existing .sto file into a Definition File.

  b) Compiling
    Using this function you can create a .sto file, with values taken from a Defintion File.
    
+) Section 4. Definition Files
==============================
SCIE reads in a "Definition File", which is simply a specially formatted text file. A commented sample file is provided in this distribution.
Definition Files are split into 6 blocks, each related to the function of a store. The blocks are entered and left using keywords:
  .sto Header
     HEADER
     ENDHEADER
  Items Sold:
     ITEMSOLD
     ENDITEMSOLD
  Spells available:
     SPELLSOLD
     ENDSPELLSOLD
  Drinks available:
     DRINKSOLD
     ENDDRINKSOLD
  Items Bought:
     ITEMBOUGHT
     ENDITEMBOUGHT
   End of file:
     EOF

Notes:
  () All values and keywords must be enclosed in < > characters.
  () Any text outside of < > characters is treated as a comment, and ignored.
  () Only the HEADER block is necessary, all other blocks are optional, though in reality at least one should be specified or the resultant store will have no use. 
  () All blocks except the HEADER block can be used multiple times. If 2 (or more) HEADER blocks are specified, the one lowest down the file takes precedence (though this is not recommended!).
  () The Definition File must be ended with an EOF marker. Anything appearing after the EOF marker is ignored.
  () Blank resource references (resref) must be entered as <>.
  () Blank string references (strref) can be entered as -1.
  () To add new text to the dialog.tlk (eg. for Store names or Drink names), enclose the text inside ~ ~ markers, as well as < > characters (eg. <~My new text~>). To signify an existing strref entry should be used, preceed the strref value with the # character (eg. <#72856>). For new text to be added to the dialog.tlk file, it is assumed that .tlk file is in the same directory as SCIE.

Read the provided sample Definition File (input.txt) for more information.

+) Section 5. Known Issues
==========================
There are no known issues at this time.
If you find any errors, please let me know immediately, specifying as much as you can about your problem.

+) Section 6. Thanks to
=======================
This tool would not have taken a lot longer to produce without:
  + IESDP - http://www.teambg.com/iesdp

  + DLTCEP by Avenger was used to check resulting files.

+) Section 7. Contact Details
=============================
SCIE related e-mail should be sent to bg2@mcwrench.com
SCIE was programmed by bt_igi / igi (Marc Wrench)