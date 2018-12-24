VVC Creator for the Infinity Engine
-----------------------------------

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
  VCC Creator for the Infinity Engine (VCIE - pronounced ick-e) is a small tool to aid in the creation of .vvc files for Infinity Engine games. Currently BG1, BG1:ToSc, BGII:SoA, BGII:ToB, IWD1 (and add-ons) are supported (ie. games using VVC V1 files), although its is likely the tool will be expanded to support the other IE games.

+) Section 2. (un)Installation
==============================
To install VCIE simply unzip icie(xx).zip (where (xx) represents the version of VCIE). Popular unzipping tools include Winzip (http://www.winzip.com/) and Filzip (http://www.filzip.com/). Once the files are extracted you can place them wherever you like. Files included in the distribution are:
  input.txt - sample Definition File
  readme.txt - this file
  icie.exe - the icie executable

To uninstall VCIE just delete the files you extracted from icie(xx).zip. The VCIE distribution includes no external dll files, and creates no registry entries.

+) Section 3. Usage
===================
VCIE runs as a console application, so there is not much of a GUI. The 2 ways of running VCIE are:
  i) Interactive (not included in this version)
    Just run (double-click) VCIE in Windows Explorer. VCIE will run interactivly, asking for the necessary information.

  ii) Command-line
    VCIE can be run from the command-line (shortcut, run dialog, DOS box, batch file). Usage in this mode is:
      VCIE [compile | decompile] input.ext output.ext
      
    If no command-line parameters are specified, VCIE will run in interactive mode.
    
The two functions of VCIE are:
  a) Decompiling
    Using this funtion you can quickly decompile an existing .vvc file into a Definition File.

  b) Compiling
    Using this function you can create a .vvc file, with values taken from a Defintion File.
    
+) Section 4. Definition Files
==============================
VCIE reads in a "Definition File", which is simply a specially formatted text file. A commented sample file is provided in this distribution.
Definition Files are split into blocks, each related to the function of the filetype. The blocks are entered and left using keywords:
  .vvc Header
     HEADER
     ENDHEADER
   End of file:
     EOF

Notes:
  () All values and keywords must be enclosed in < > characters.
  () Any text outside of < > characters is treated as a comment, and ignored.
  () All blocks except the HEADER block can be used multiple times. If 2 (or more) HEADER blocks are specified, the one lowest down the file takes precedence (though this is not recommended!).
  () The Definition File must be ended with an EOF marker. Anything appearing after the EOF marker is ignored.
  () Blank resource references (resref) must be entered as <>.
  () Blank string references (strref) can be entered as -1.

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
VCIE related e-mail should be sent to bg2@mcwrench.com
VCIE was programmed by bt_igi / igi (Marc Wrench)