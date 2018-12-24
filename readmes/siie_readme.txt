Store Inserter for the Infinity Engine
-------------------------------------

+) Contents
===========
1.    About
2.    (Un)Installation
3.    Usage
4.    Definition Files
5.    Known Issues
6.	Still to do
7.    Thanks to
8.    Contact Details

+) Section 1. About
===================
  Store Inserter for the Infinity Engine (SIIE - pronounced sigh) is a small tool to aid in the distribution of .sto files for Infinity Engine games. Currently only Baldurs Gate II (SOA or TOB) is supported, although its is likely the tool will be expanded to support the other IE games.

+) Section 2. (un)Installation
==============================
To install SIIE simply unzip siie[xx].zip (where [xx] represents the version of SIIE). Popular unzipping tools include Winzip (http://www.winzip.com/) and Filzip (http://www.filzip.com/). Once the files are extracted you can place them wherever you like. Files included in the distribution are:
  readme.txt - this file
  siie.exe - the siie executable

To uninstall SIIE just delete the files you extracted from siie[xx].zip. The SIIE distribution includes no external dll files, and creates no registry entries.

+) Section 3. Usage
===================
SIIE runs as a console application, so there is not much of a GUI. The 2 ways of running SIIE are:
  i) Interactive (not included in this version)
    Just run (double-click) SIIE in Windows Explorer. SIIE will run interactivly, asking for the necessary information.

  ii) Command-line
    SIIE can be run from the command-line (shortcut, run dialog, DOS box). Usage in this mode is:
        SIIE [(a|r)gentle | (a|r)force ] inFile.ext outFile.ext
      
    If no command-line parameters are specified, SIIE will run in interactive mode.
    
The two functions of SIIE are:
  a) Inserting (agentle & aforce)
    Using this funtion you can insert items/spells/drinks into an existing store. The agentle switch means that objects will only be added to the .sto if no existing object with the same name exists. The aforce switch means that an object in the .sto will be overwitten if an object exists in the Definition file with the same name.

  b) Compiling (rgentle & rforce)
    Using this funtion you can delete items/spells/drinks into an existing store. The rgentle switch means that objects will only be removed from the .sto if the entire object matches (eg. name, price, stock etc). The rforce switch means that object will be removed from the .sto based solely on the filename.
    
+) Section 4. Definition Files
==============================
SIIE reads in a "Definition File", which is simply a specially formatted text file. A commented sample file is provided in this distribution.
Definition Files are split into 6 blocks, each related to the function of a store. The blocks are entered and left using keywords:
  .sto Header
     BEGINHEADER
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
  () Only the HEADER block is necessary, all other blocks are optional, though in reality at least one should be specified or the resultant store will have no use. 
  () All blocks except the HEADER block can be used multiple times. If 2 (or more) HEADER blocks are specified, the one lowest down the file takes precedence (though this is not recommended!).
  () At all times in the Definition File the semi-colon (;) character acts as a comment marker, marking the rest of that line as a comment (which is ignored when parsing the Definition File).
  () The Definition File must be ended with an EOF marker. Anything appearing after the EOF marker is ignored.
  () Blank resource references (resref) must be entered as <>.
  () Blank string references (strref) can be entered as -1.
  () For the Store Name string reference, new text can be added to the tlk file, or an existing string reference can be stated. To use an existing reference, preceed the strref number with a # (eg. #72856). To add new text, surround it with the ~ character (eg. ~My store name~). If new text is to be added to the dialog.tlk file, it is assumed that .tlk file is in the same directory as SIIE.
  () Whitespace (spaces and tabs) can be used to aid clarity of the Definition File. Whitespace can be used everywhere except within keywords,values, and definitions (ie. item entries, spell entries etc must appear on one line):
  Keywords	eg1. ITEMBOUGHT will read as "ITEMBOUGHT" (valid)
                 ITEM  BOUGHT will read a "ITEM" and "BOUGHT" (invalid)

  Value	eg2. 17 will read as "17" (valid)
                 1    7 will read as "1" and "7" (invalid)

  Value	eg3. RFRIEND will read as "RFRIEND" (valid)
                 R FREIN  D will read as "R" and "FRIEN" and "D" (invalid)

Read the provided sample Definition File (input.txt) for more information.
NB. SIIE uses the same Definition File format as SCIE.

+) Section 5. Known Issues
==========================
There are no known issues at this time.
NB. This tool has had very little testing, be sure to make back-ups of your work.
If you find any errors, please let me know immediately, specifying as much as you can about your problem.

+) Section 7. Still to do
=========================
Future versions will allow:
  Checks on input
  Interactive mode
  New strings to be added for Drink Names
  Support for BG1, IWD, IWD2
  Testing

+) Section 7. Thanks to
=======================
This tool would not have taken a lot longer to produce without:
  + IESDP - http://www.teambg.com/iesdp

  + DLTCEP by Avenger was used to check resulting files (insead of loading BG2).

+) Section 8. Contact Details
=============================
ECIE related e-mail should be sent to igi@teambg.net
ECIE was programmed by bt_igi / igi (Marc Wrench)