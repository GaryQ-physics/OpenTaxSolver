Open Tax Solver - Package
--------------------------

August 19, 2022 v19.08 - For 2021 tax-year.

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
	  the 2021 Tax-Year.
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
    * v19.08 (8/19/202) - Compilation of remedial revisions from last several months.
	  On CA_540, fixed printing of multiple dependent names, and added question about Use-Tax payments.
	  On Massachusetts form, removed lines 12+13, which are not used in 2021.
	  On HSA Form 8889, now set line-6 to line-5 value, if no value is specified on line-6.
    * v19.07 (3/27/2022) - Added check for matching input Form-types.
	  Checks that input files match the selected Program to run.
	  In case of mismatch, it now displays a warning message.
	  On Fed-1040, adjusted the limit to charitable deductions for
	  non-married filers who are not optimizing.
    * v19.06 (3/3/2022) - Clarified where to enter Charity Donations on
	  the Federal 1040 form, by creating designated Charity line.
	- For MacOS platforms, added MacSetup command file for allowing
	  operation under the increased security restrictions of MacOS
	  Catalina (10.15), Big Sur (11), Monterey (12), and beyond.
	  On MacOS, run 'MacSetup' once, before running the OTS-GUI.
    * v19.05 (2/24/2022) - In California state form, added County-name and
	  check-box for Same-Residence address on first PDF page.
	- Improved informational message in Fed-1040, and NJ-1040 programs.
    * v19.04 (2/17/2022) - Added complete NY state IT-196 form for
	  limited itemized deductions to the NY-IT201 program.  
	  The program will add to PDF fill-out when needed.
	- Revised California form 5805 Question-4 condition.
    * v19.03 (2/11/2022) - Fixed NY state line 18 input from Fed Sched-1.
	- Updates to California form 5805 and examples.
	- Updates to California form 540 PDF printout of Single name and initial.
    * v19.02 (2/07/2022) - Fixed Fed-1040 std-deduction for single filers.
	- Added Health-Insurance checkbox to CA-540 state form.
	- Updated Form 2210.
    * v19.01 (2/04/2022) - Update to charitable donations limit in
	and the age-65 comment in Federal-1040 form.
	- Updated California state tax program (540) for 2021 tax-year.
	- Updated California form 5805.
	- Updated forms 2201, 8959, and 8960.
	- Added a notify-popup utility that can be used by all 
	  programs for alerting users of any detected issues.
	- Now GUI will not offer to fill-out PDF forms if there
	  are any errors detected in the compute step, and it
	  will pop-up an alert window, so error is not missed.
    * v19.00 (1/29/2022) - Preliminary release for Tax-Year 2021.
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
template to a new name, such as "fed1040_2021.txt".  After filling-in the
lines, then run the tax solver on it.  From the GUI, this is done by
pressing "Compute Tax" button.
Or solvers can be run from the command-line, for example, as:
  bin/taxsolve_usfed1040_2021  Fed1040_2021.txt
Where "Fed1040_2021.txt" is the name of -your- tax-data file, which
you can edit with your favorite text-editor to fill it in or print
it out.  Output results are saved to "..._out.txt" files
(eg. Fed1040_2021_out.txt), and can be printed out directly too.

For updates and further information, see:
        http://sourceforge.net/projects/opentaxsolver/
Documentation:
        http://opentaxsolver.sourceforge.net/

Re-compiling:
 Unix/Linux/Mac:
  Pre-compiled executables for Unix/Linux are normally in bin directory.
  However to build the binaries in the bin/ directory:
     cd OpenTaxSolver2021_19.xx	      ( cd into top directory. )
     rm ./bin/* Run_taxsolve_GUI      ( Clears executables. )
     src/Build_taxsolve_packages.sh   ( Creates executables. )

 MS-Windows:
   Pre-compiled executables are normally in bin directory.
   For compiling OTS on MSwindows, MinGW with Msys is recommended.
   From Msys terminal window:
      cd OpenTaxSolver2021_18.xx       ( cd into top directory. )
      rm ./bin/* Run_taxsolve_GUI.exe  ( Clears executables. )
      src/Build_taxsolve_packages.sh   ( Creates executables. )

Directory Structure:
OpenTaxSolver2021       ......................................       25.246-KB
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
