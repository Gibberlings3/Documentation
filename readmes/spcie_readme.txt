Spell Creator for the Infinity Engine
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
  Spell Creator for the Infinity Engine (SPCIE - pronounced Spikey) is a small tool to aid in the creation of .spl files for Infinity Engine games. Currently only BG1, BG1:ToSc, BGII:SoA, BGII:ToB and IWD1 (with add-ons) are supported (ie. games using SPL V1 files), although its is likely the tool will be expanded to support the other IE games.

+) Section 2. (un)Installation
==============================
To install SPCIE simply unzip spcie(xx).zip (where (xx) represents the version of SPCIE). Popular unzipping tools include Winzip (http://www.winzip.com/) and Filzip (http://www.filzip.com/). Once the files are extracted you can place them wherever you like. Files included in the distribution are:
  input.txt - sample Definition File
  readme.txt - this file
  spcie.exe - the spcie executable

To uninstall SPCIE just delete the files you extracted from spcie(xx).zip. The SPCIE distribution includes no external dll files, and creates no registry entries.

+) Section 3. Usage
===================
SPCIE runs as a console application, so there is not much of a GUI. The 2 ways of running SPCIE are:
  i) Interactive (not included in this version)
    Just run (double-click) SPCIE in Windows Explorer.

  ii) Command-line
    SPCIE can be run from the command-line (shortcut, run dialog, DOS box, batch file). Usage in this mode is:
      SPCIE [compile | decompile] input.ext output.ext

The two functions of SPCIE are:
  a) Decompiling
    Using this funtion you can quickly decompile an existing .spl file into a Definition File.

  b) Compiling
    Using this function you can create a .spl file, with values taken from a Defintion File.
    
+) Section 4. Definition Files
==============================
SPCIE reads in a "Definition File", which is simply a specially formatted text file. A commented sample file is provided in this distribution.
Definition Files are split into blocks, each related to the a section of a spell. The blocks are entered and left using keywords:
  .spl Header
     HEADER
     ENDHEADER
   Extended Header
     EXTENDEDHEADER
     ENDEXTENDEDHEADER
   Feature Block
     FEATUREBLOCK
     ENDFEATUREBLOCK
   End of file:
     EOF

Notes:
  () All values and keywords must be enclosed in < > characters.
  () Any text outside of < > characters is treated as a comment, and ignored.
  () Only the HEADER block is necessary, all other blocks are optional, though in reality at least one should be specified or the resultant spell will have no use. 
  () All blocks except the HEADER block can be used multiple times. If 2 (or more) HEADER blocks are specified, the one lowest down the file takes precedence (though this is not recommended!).
  () To add feature blocks to extended headers, simply start a FEATUREBLOCK inside an EXTENDEDHEADER, as demonstrated in the sample Definition File.
  () The Definition File must be ended with an EOF marker. Anything appearing after the EOF marker is ignored.
  () Blank resource references (resref) must be entered as <>.
  () Blank string references (strref) can be entered as -1.
  () To add new text to the dialog.tlk (eg. for parameters, or spell names/descriptions), enclose the text inside ~ ~ markers, as well as < > characters (eg. <~My new text~>). To signify an existing strref entry should be used, preceed the strref value with the # character (eg. <#72856>). For new text to be added to the dialog.tlk file, it is assumed that .tlk file is in the same directory as SCIE.

Read the provided sample Definition File (input.txt) for more information.

+) Section 5. Known Issues
==========================
When decompiling, comments are not always aligned correctly.

If you find any errors, please let me know immediately, specifying as much as you can about your problem.

+) Section 6. Thanks to
=======================
This tool would not have taken a lot longer to produce without:
  + IESDP - http://www.teambg.com/iesdp

  + DLTCEP by Avenger was used to check resulting files.

+) Section 7. Contact Details
=============================
SPCIE related e-mail should be sent to bg2@mcwrench.com
SPCIE was programmed by bt_igi / igi (Marc Wrench)