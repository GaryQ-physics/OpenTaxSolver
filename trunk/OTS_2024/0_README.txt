Open Tax Solver - Package
--------------------------

March 14, 2025 v22.06 - For Tax-Year 2024.

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
	  the 2024 Tax-Year.
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
    * v22.06 (3/15/2025) - Switched formatting of Fed-1040, and related 
	Federal Forms to Round-to-Whole dollars.  Added ability to fill-in 
	PIN numbers in Fed-1040.  Added ability to check request for Health
	info on the CA-540 PDF Form.  Updated the Form 8829 template.  
	Added initial version of Oregon State tax form program.
    * v22.05 (3/6/2025) - Promoted the new MI State form to front GUI panel.
	Fixed the new MI State form line 34.  In OH State form's optional
	information section, added second address line, and county-code.
	In AZ State form, now sets line 29a limit according to the number
	of tax-payers.  Removed quotes around Dependent names in Form-1040
	output to ease parsing in new form programs using 1040 output.
    * v22.04 (2/28/2025) - The PDF fill-out program can now suppress
	negative signs for form-lines enclosed in parenthesis, which
	are expected to be negative (by accounting notation).
	As for example on Schedule-D, lines 14 and 21. 
	Added Fed-1040 Sched-D lines 1a and 8a, for those who receive
	Forms 1099-B on some transactions.
    * v22.03 (2/12/2025) - Fixed stray comma in Fed 1040 and 2210 tax-table.
	Added click-able instructions for forms 8602, 8812, 8895, 8959, and 8960.
	Added option in GUI to set a custom save-directory instead of the default,
	Invoke ots_gui with command-line option '-help' to see the option(s).
    * v22.02 (2/6/2025) - Added initial preliminary version of Michigan
	  State tax form.
	- Added options to Run_taxsolve_GUI for enlarging window and text
	  for Hi-DPI screens. (Invoke Run_taxsolve_GUI with '-large'.)
	- Added entries for fed-1040 to enter refund direct deposit info.
    * v22.01 (1/30/2025) - Added the NY State PDF form.
	- Updated Federal Form F2210, and CA-540 State programs.
    * v22.00 (1/27/2025) - Preliminary release for Tax-Year 2024.
	- Includes updates for many of the run-able forms.
	- Although the tax-program for NY State has been updated, we are
	  still waiting for Dept of Taxation to post NY's PDF Form.
	- Please check back for more updates.

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
template to a new name, such as "fed1040_2024.txt".  After filling-in the
lines, then run the tax solver on it.  From the GUI, this is done by
pressing "Compute Tax" button.
Or solvers can be run from the command-line, for example, as:
  bin/taxsolve_usfed1040_2024  Fed1040_2024.txt
Where "Fed1040_2024.txt" is the name of -your- tax-data file, which
you can edit with your favorite text-editor to fill it in or print
it out.  Output results are saved to "..._out.txt" files
(eg. Fed1040_2024_out.txt), and can be printed out directly too.

For updates and further information, see:
        http://sourceforge.net/projects/opentaxsolver/
Documentation:
        http://opentaxsolver.sourceforge.net/

Re-compiling:
 Unix/Linux/Mac:
  Pre-compiled executables for Unix/Linux are normally in bin directory.
  However to build the binaries in the bin/ directory:
     cd OpenTaxSolver2024_22.xx	      ( cd into top directory. )
     rm ./bin/* Run_taxsolve_GUI      ( Clears executables. )
     src/Build_taxsolve_packages.sh   ( Creates executables. )

 MS-Windows:
   Pre-compiled executables are normally in bin directory.
   For compiling OTS on MSwindows, MinGW with Msys is recommended.
   From Msys terminal window:
      cd OpenTaxSolver2024_18.xx       ( cd into top directory. )
      rm ./bin/* Run_taxsolve_GUI.exe  ( Clears executables. )
      src/Build_taxsolve_packages.sh   ( Creates executables. )

Directory Structure:
OpenTaxSolver2024       ......................................       25.246-KB
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
