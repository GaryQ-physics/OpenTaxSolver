Open Tax Solver - North Carolina State D-400 Personal Income Tax Return
-----------------------------------------------------------------------

Included here is a program, template, and example for
North Carolina State D-400 personal income tax form.
Intended for use with the NC D-401 Instructions Booklet.

The NC400_2024_example.txt files is included for testing.
The NC400_2024_template.txt file is a blank starting form for
entering your tax data.  For each filer, copy template to a new
name, such as "NC400_2024.txt" or "NC400_2024_aunt_sally.txt,
and fill-in the lines.

The program consists of two files:
  taxsolve_NC400_2024.c - main, customized for NC D-400.
  taxsolve_routines.c - general purpose base routines.

Compile:
  cc taxsolve_NC400_2024.c -o taxsolve_NC400_2024

Run:
 First, run your Federal 1040 taxes and note the output file.
  ../../bin/taxsolve_fed1040_2024 fed1040_2024.txt 
 Then, complete your NC400 form input data file and run.
  ../../bin/taxsolve_NC400_2024  NC400_2024.txt


For updates and further information, see:
        http://sourceforge.net/projects/opentaxsolver/
Documentation:
        http://opentaxsolver.sourceforge.net/


Contributed by S. Jenkins 
Updated by Lincoln Baxter for 2007 (lab@lincolnbaxter.com)
Updated by ARoberts for 2008-2024 (aston_roberts@yahoo.com)
