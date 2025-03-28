Open Tax Solver - Package
--------------------------

April 18, 2024 v21.06 - For Tax Year 2023.

See project homepage:	http://opentaxsolver.sourceforge.net/

OpenTaxSolver (OTS) is a set of programs and templates for helping you
fill out your income tax forms.  It performs the tedious arithmetic.
OTS is intended to assist those who normally prepare their tax forms
themselves, and who generally know on which lines to enter their numbers.
It is meant to be used in combination with the instruction booklet 
corresponding to a given form.

This package contains programs and templates for:
	- US-1040 - which also does the Schedules A, B, D, and forms 8949. 
	- Schedule C for US-1040.
	- State Income Taxes for Ohio, New Jersey, Virginia, Pennsylvania,
	  Massachusetts, North Carolina, and California taxes updated for
	  the 2023 Tax-Year.
Also contains an Automatic PDF Form-Fillout function:
	- Supports all Federal Forms and State Forms.
	  Saves time by filling out many of the numbers.  
	  You may still need to enter some information or check boxes
	  that are not handled by OTS.
	  Tested to work properly with many PDF viewers.
	- You can edit your forms with Libre-Office.

-----------------------------------------------------------
--- This package contains executables for RPLCSTRNG_01 ---
-----------------------------------------------------------
  RPLCSTRNG_02

History:
    * v21.06 (4/18/2024) - To Massachusetts State Form, added 
		Line-6b for Farm income, and made Business income
		Line-6a show up on PDF form.
		Clean re-compile of all the intervening updates
		since the prior full release.
    * v21.05c (4/9/2024) - Added to Virginia State the ability to
		enter Spouse VAGI so that it shows up on PDF form.
    * v21.05b (4/6/2024) - Fix to AZ State for filing Single to
		accept line 4a by default.
    * v21.05a (4/5/2024) - Fix to NY State line 7 for the case
		when there are net Capital Losses. 
    * v21.05 (4/2/2024) - Fix to Fed 1040 Qualified Dividends and 
		Capital Gain Tax Worksheet line 3, for when not
		filing Schedule-D.
    * v21.04 (3/14/2024) - Completed updating Ohio State Form line
		changes for 2023 tax year.
		Updated Massachusetts State Taxes Line 14 maximum 
		rental deduction for 2023.  Some other small
		form clean-ups.
    * v21.03 (3/3/2024) - Small fixes to output Form files for 
		US_1040, CA_540, and US_1040_Sched_C.
		Fixed placement of US_1040_Sched_C Line 27a in the
		PDF output.
    * v21.02 (2/14/2024) - Fixes to CA Form-5808 for 2023 updates
		with added WorkSheets in PDF output.
		Adjusted Makefile for compilation on Raspberry-Pi.
		Added initial version of Sched-8, Form-8812 for
		"Credits for Qualifying Children and Dependents",
		for preliminary testing.
    * v21.01 (2/11/2024) - In California 540 Adjustments Part II,
		removed line 8d from template and example files,
		which no longer applies for 2023 taxes.
    * v21.00 (2/4/2024) - Preliminary release for Tax-Year 2023.
		Please check back for updates.

Usage:
 RPLCSTRNG_03
  (Located in the top directory.)
 RPLCSTRNG_04
 For Auto-Fillout of PDF Forms, click the "Print" button, and select
  "Automatically Fill-out PDF Tax-Form", then click "Print".
 You can set your preferred PDF viewer by the (Set PDF Viewer) button,
  or by setting the environment variable:  PDF_VIEWER
 The Auto-Fillout feature is tested to work properly with the PDF
 viewers "Google-Chrome", "Firefox", "LibreOffice", "Atril", "Xpdf", 
 "Safari", "IE", "Edge", and "Acrobat Reader".
 You can edit your filled-out PDF forms with LibreOffice.

General:
Example tax-data files and blank starting templates are included under
the "tax_form_files" directory.  For each filer, save filled-out 
template to a new name, such as "fed1040_2023.txt".  After filling-in the
lines, then run the tax solver on it.  From the GUI, this is done by
pressing "Compute Tax" button.
Or solvers can be run from the command-line, for example, as:
  bin/taxsolve_usfed1040_2023  Fed1040_2023.txt
Where "Fed1040_2023.txt" is the name of -your- tax-data file, which
you can edit with your favorite text-editor to fill it in or print
it out.  Output results are saved to "..._out.txt" files
(eg. Fed1040_2023_out.txt), and can be printed out directly too.

For updates and further information, see:
        http://sourceforge.net/projects/opentaxsolver/
Documentation:
        http://opentaxsolver.sourceforge.net/

Re-compiling:
 Unix/Linux/Mac:
  Pre-compiled executables for Unix/Linux are normally in bin directory.
  However to build the binaries in the bin/ directory:
     cd OpenTaxSolver2023_19.xx	      ( cd into top directory. )
     rm ./bin/* Run_taxsolve_GUI      ( Clears executables. )
     src/Build_taxsolve_packages.sh   ( Creates executables. )

 MS-Windows:
   Pre-compiled executables are normally in bin directory.
   For compiling OTS on MSwindows, MinGW with Msys is recommended.
   From Msys terminal window:
      cd OpenTaxSolver2023_18.xx       ( cd into top directory. )
      rm ./bin/* Run_taxsolve_GUI.exe  ( Clears executables. )
      src/Build_taxsolve_packages.sh   ( Creates executables. )

Directory Structure:
OpenTaxSolver2023       ......................................       25.246-KB
   |-- src   .................................................      217.555-KB
   |   |-- Gui_gtk   .........................................      141.807-KB
   |
   |-- tax_form_files   ......................................       49.152-KB
   |   |-- VA_760   ..........................................       11.038-KB
   |   |-- US_1040_Sched_C   .................................       12.803-KB
   |   |-- US_1040   .........................................       21.351-KB
   |   |-- PA_40   ...........................................       11.562-KB
   |   |-- OH_1040   .........................................       14.860-KB
   |   |-- NY_IT201   ........................................       14.686-KB
   |   |-- NJ_1040   .........................................       14.124-KB
   |   |-- NC_400   ..........................................       12.251-KB
   |   |-- MA_1   ............................................       13.844-KB
   |   |-- CA_540   ..........................................       13.166-KB
   |
   |-- bin   .................................................      351.033-KB
16 Directories.

---------------------------------------------------------------------------------
Aston Roberts (aston_roberts@yahoo.com)
File Organization and Makefiles by: Krish Krothapalli, David Masterson, & Jesse Becker
Programs contain contributions by many others.  See OTS credits webpage.
