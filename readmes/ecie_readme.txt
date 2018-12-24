EFF Creator for the Infinity Engine
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
  EFF Creator for the Infinity Engine (ECIE - pronounced e-key) is a small tool to aid in the creation of .eff files for Infinity Engine games. Currently BG1:ToSc, BGII:SoA and BGII:ToB, IWD1 (and add-ons) are supported (ie. games using EFF V2 files), although its is likely the tool will be expanded to support the other IE games.

+) Section 2. (un)Installation
==============================
To install ECIE simply unzip ecie(xx).zip (where (xx) represents the version of ECIE). Popular unzipping tools include Winzip (http://www.winzip.com/) and Filzip (http://www.filzip.com/). Once the files are extracted you can place them wherever you like. Files included in the distribution are:
  input.txt - sample Definition File
  readme.txt - this file
  ecie.exe - the ecie executable

To uninstall ECIE just delete the files you extracted from ecie(xx).zip. The ECIE distribution includes no external dll files, and creates no registry entries.

+) Section 3. Usage
===================
ECIE runs as a console application, so there is not much of a GUI. The 2 ways of running ECIE are:
  i) Interactive (not included in this version)
    Just run (double-click) ECIE in Windows Explorer. ECIE will run interactivly, asking for the necessary information.

  ii) Command-line
    ECIE can be run from the command-line (shortcut, run dialog, DOS box, batch file). Usage in this mode is:
      ECIE [compile | decompile] input.ext output.ext
      
    If no command-line parameters are specified, ECIE will run in interactive mode.
    
The two functions of ECIE are:
  a) Decompiling
    Using this funtion you can quickly decompile an existing .eff file into a Definition File.

  b) Compiling
    Using this function you can create a .eff file, with values taken from a Defintion File.
    
+) Section 4. Definition Files
==============================
ECIE reads in a "Definition File", which is simply a specially formatted text file. A commented sample file is provided in this distribution.
Definition Files are split into blocks, each related to the function of the filetype. The blocks are entered and left using keywords:
  .eff Header
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
  () To add new text to the dialog.tlk (eg. for parameters), enclose the text inside ~ ~ markers, as well as < > characters (eg. <~My new text~>). To signify an existing strref entry should be used, preceed the strref value with the # character (eg. <#72856>). For new text to be added to the dialog.tlk file, it is assumed that .tlk file is in the same directory as ECIE.

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
ECIE related e-mail should be sent to bg2@mcwrench.com
ECIE was programmed by bt_igi / igi (Marc Wrench)