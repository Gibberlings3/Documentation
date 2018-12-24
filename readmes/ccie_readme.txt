Creature Creator for the Infinity Engine
----------------------------------------

+) Contents
===========
1.    About
2.    (Un)Installation
3.    Usage
4.    Definition Files
5.    Known Issues
6.    Still to do
7.    Thanks to
8.    Contact Details

+) Section 1. About
===================
  Creature Creator for the Infinity Engine (CCIE - Cre-key) is a small tool to aid in the creation of .cre files for Infinity Engine games. Currently only Baldurs Gate I (inc. TotS) and Baldurs Gate II (SOA or TOB) are supported, although its is possible the tool will be expanded to support the other IE games.

+) Section 2. (un)Installation
==============================
To install CCIE simply unzip ccie(xx).zip (where [xx] represents the version of CCIE). Popular unzipping tools include Winzip (http://www.winzip.com/) and Filzip (http://www.filzip.com/). Once the files are extracted you can place them wherever you like. Files included in the distribution are:
  notes.txt - further notes/info
  input.txt - sample Definition File
  readme.txt - this file
  ccie.exe - the ccie executable

To uninstall CCIE just delete the files you extracted from ccie[xx].zip. The CCIE distribution includes no external dll files, and creates no registry entries.

+) Section 3. Usage
===================
CCIE runs as a console application, so there is not much of a GUI. The 2 ways of running CCIE are:
  i) Interactive (not included in this version)
    Just run (double-click) CCIE in Windows Explorer. CCIE will run interactivly, asking for the necessary information.

  ii) Command-line
    CCIE can be run from the command-line (shortcut, run dialog, DOS box). Usage in this mode is:
      CCIE [compile | decompile] input.ext output.ext
      
    If no command-line parameters are specified, CCIE will run in interactive mode.
    
The two functions of CCIE are:
  a) Decompiling
    Using this funtion you can quickly decompile an existing .cre file into a Definition File.

  b) Compiling
    Using this function you can create a .cre file, with values taken from a Defintion File.
    
+) Section 4. Definition Files
==============================
CCIE reads in a "Definition File", which is simply a specially formatted text file. A commented sample file is provided in this distribution.
Definition Files are split into blocks, each related to the function of a store. The blocks are entered and left using keywords:
  .cre Header
     HEADER
     ENDHEADER
  Spells Known:
     SPELLBOOK
     ENDSPELLBOOK
  Spell Memorisation Info:
     SPELLSOLD
     ENDSPELLINFO
  Spells Memorised:
     SPELLMEM
     ENDSPELLMEM
  Items:
     ITEM
     ENDITEM
   Effects:
     EFFECT
     ENDEFFECT
   End of file:
     EOF

Notes:
  () All values and keywords must be enclosed in < > characters.
  () Any text outside of < > characters is treated as a comment, and ignored.
  () Only the HEADER block is necessary, all other blocks are optional.
  () All blocks except the HEADER block can be used multiple times. If 2 (or more) HEADER blocks are specified, the one lowest down the file takes precedence (though this is not recommended!).
  () The Definition File must be ended with an EOF marker. Anything appearing after the EOF marker is ignored.
  () Blank resource references (resref) must be entered as <>.
  () Blank string references (strref) can be entered as -1.
  () To add new text to the dialog.tlk (eg. for parameters, or spell names/descriptions), enclose the text inside ~ ~ markers, as well as < > characters (eg. <~My new text~>). To signify an existing strref entry should be used, preceed the strref value with the # character (eg. <#72856>). For new text to be added to the dialog.tlk file, it is assumed that .tlk file is in the same directory as CCIE.
  () It is easy to produce invalid file using CCIE, espcially regarding spells. It is suggested you decompile several files and study the resultant Definition Files before editing them.

Read the provided sample Definition File (input.txt) for more information.

+) Section 5. Known Issues
==========================
There are no known issues at this time.
If you find any errors, please let me know immediately, specifying as much as you can about your problem.

+) Section 7. Still to do
=========================
Future versions will allow:
  Checks on input
  Interactive mode
  Support for other CRE file versions

+) Section 7. Thanks to
=======================
This tool would not have taken a lot longer to produce without:
  + IESDP - http://www.teambg.com/iesdp

  + DLTCEP by Avenger was used to check resulting files (insead of loading BG2).

+) Section 8. Contact Details
=============================
The CCIE homepage is http://www.teambg.net/~igi
CCIE related e-mail should be sent to igi@teambg.net
CCIE was programmed by bt_igi / igi (Marc Wrench)