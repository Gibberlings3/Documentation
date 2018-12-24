.IAP Unpacker
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
  IAPU is a small tool to unpack files which have been packaged in the .IAP format. Rather than requring loading of a program, and the use of commands in layers of menu's, or running a self-extracting archive, IAPU allows the contained files to be quickly extracted to the current directory, preserving relative directories. Text associated with the contained files is not extracted, and is not added to the dialog.tlk file.

+) Section 2. (un)Installation
==============================
To install IAPU simply unzip iapu(xx).zip (where (xx) represents the version of IAPU). Popular unzipping tools include Winzip (http://www.winzip.com/) and Filzip (http://www.filzip.com/). Once the files are extracted you can place them wherever you like. Files included in the distribution are:
  readme.txt - this file
  iapu.exe - the iapu executable
  unpack.bat - batch file for auto-unpacking of extracted .tbg fils

To uninstall IAPU just delete the files you extracted from iapu(xx).zip. The IAPU distribution includes no external dll files, and creates no registry entries.

+) Section 3. Usage
===================
IAPU runs as a console application, so there is not much of a GUI. The 2 ways of running IAPU are:
  i) Interactive (not included in this version)
    Just run (double-click) IAPU in Windows Explorer. IAPU will run interactivly, asking for the necessary information.

  ii) Command-line
    IAPU can be run from the command-line (shortcut, run dialog, DOS box, batch file). Usage in this mode is:
      IAPU input.iap
      
    If no command-line parameters are specified, IAPU will run in interactive mode.

.tbg files contained in the .iap archive will be unpacked, but left as .tbg files. A separate .tbg importing uility must be used to unpack these .tbg files. The included batch file (unpack.bat) uses the TBGU utility (available at the same location as this program), to unpack all the .tbg files in the current directory. To use this bat file, simply place TBGU, IAPU and unpack.bat in the same location, and drag the .iap file onto the unpack.bat file. IAPU will be invoked, unpacking the .tbg and other files, then TBGU will be invoked, unpacking the .tbg files.
    
NB: Associated text is not extratced, and is not added to the dialog.tlk file. This means the any text used inthe item file will likely be incorrect. However, this also means you can quickly extract files without worrying about cluttering up the .tlk file, remebering to make backups, or remembering to remove files from the override directory. IAPU is meant as a quick extraction tool, so allow you to see how the files inside .iap archives work, without requring full installation of the archive.

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
IAPU related e-mail should be sent to bg2@mcwrench.com
IAPU was programmed by bt_igi / igi (Marc Wrench)