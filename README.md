CADCompare
==========

Version: 0.26.0 [Download](https://github.com/dibeneditto/cadcompare/blob/master/releases/win32/CADcompare-win32-v0.26.0.zip)

Release Date: 2017-05-11

[Sourcecode](https://github.com/dibeneditto/cadcompare)

CADCompare is a program that finds the differences in CAD PDF files.
This version runs as a Windows Batch file (CMD file), which depending
on your system security you may need permission from your system
administrator to run it. Please see the REQUIREMENTS section below.


BASED ON PUBLISHED RESEARCH
---------------------------

CADcompare™: A Web-based Application that Compares PDF CAD Drawings
Jun 2018
American Society for Education Engineering (ASEE) Engineering Design Graphics Division 2018 ASEE Annual Conference & Exposition
Lukas DiBeneditto, Rustin Webster

This work in progress describes the development of a web application titled CADcompare™, which automatically compares, displays, and highlights differences in Portable Document Format (PDF) files of computer-aided design (CAD) drawings and is specifically designed to compare multiple student files to an instructor's grading key. CADcompare augments the grading process of technical and engineering CAD drawings by highlighting differences that can be easily missed by a human grader, such as incorrect line type(s), color(s), or double lines (i.e., lines on top of each other). Some CAD software has built-in comparison tools, however, none of the comparison tools accept PDF files to compare, are web-based applications, or can compare multiple student files at once like CADcompare can. Grading engineering CAD drawings with accuracy and fairness can take a lot of time, the intended use of CADcompare is to act as a grading tool to help instructors grade faster, more accurately, and without unintended bias. Spring 2017, a Windows® based proof of concept version of CADcompare installed on a personal computer showcased the strengths of the software. CADcompare was able to compare multiple student drawings to the grading key much faster than previously used methods. Outcomes from user testing prompted the current development of a web-based version. This paper offers general details on how CADcompare compares PDF files, market analysis, the work in progress, and a planned research study comparing grading times with and without CADcompare in an introductory engineering graphics course.

[https://peer.asee.org/30121](https://peer.asee.org/30121)


HOW IT WORKS
------------

The program compares the files in the "studentpdfs" folder to the file
in the "teacherkey" folder and creates new files highlighting the
differences in the "results" folder.


INSTRUCTIONS
------------

To run this program:

1. Put the teacher's grading key PDF file in the "teacherkey" folder.
   - There can be only one file in this folder.

2. Put the student PDF file(s) in the "studentpdfs" folder.

3. Doubleclick "cadcompare" or run it from the command line.

4. Follow the interactive instructions for how you want the results.

5. New files highlighting the differences will be in the "results"
   folder.

6. NOTE: Any files in the "results" folder will be OVER WRITTEN if they
   have the same file name. To prevent this move the files out of the
   "results" folder before running the program again.

   Example:

       BEFORE first run of program:
           
         - teacherkey (folder)

           - teacherkey-assignment1-problem1.pdf

         - studentpdfs (folder)

           - james-smith-1-1.pdf
           - mary-johnson-1-1.pdf

         - results (folder)

           - (no files yet)

       AFTER first run of program, BEFORE second run of program:

         - teacherkey (folder)

           - teacherkey-assignment1-problem1.pdf

         - studentpdfs (folder)

           - james-smith-1-1.pdf
           - mary-johnson-1-1.pdf

         - results (folder)

           - james-smith-1-1-diff.pdf
           - mary-johnson-1-1-diff.pdf

       AFTER second run of program:

         - teacherkey (folder)

           - teacherkey-assignment1-problem1.pdf

         - studentpdfs (folder)

           - james-smith-1-1.pdf
           - mary-johnson-1-1.pdf

         - results (folder)

           - james-smith-1-1-diff.pdf (file was OVER WRITTEN)
           - mary-johnson-1-1-diff.pdf (file was OVER WRITTEN)


SUGGESTIONS ON FILE NAMES
-------------------------

  teacherkey-assignment1-problem1.pdf
  james-smith-1-1.pdf
  mary-johnson-1-1.pdf

  teacherkey-assignment2-problem3.pdf
  james-smith-2-3.pdf
  mary-johnson-2-3.pdf


PREMISE
-------

If a group of students are using the same type of computer, the same
software, and follow the directions to "plot" or print a CAD drawing,
then any differences can be found using software by pixel comparison.

Since the teacher key PDF file and the student PDF file should be the
same, excluding certain areas in the title block like the name and date,
any differences can be highlighted by software.


REQUIREMENTS
------------

Windows 32 bit or higher

PDF files

- Must be only 1 page.

- Must be the same page size.

  - Example: file1.pdf 8x11, file2.pdf 8x11, correct
  - Example: file1.pdf 8x11, file2.pdf 11x17, incorrect different
    page sizes.

- Must be the same page orientation.

  - Example: file1.pdf 8x11, file2.pdf 8x11, correct
  - Example: file1.pdf 8x11, file2.pdf 11x8, incorrect different
    page orientation, file1.pdf is portrait, file2.pdf is landscape.

  - Example: file1.pdf 11x8, file2.pdf 11x8, correct
  - Example: file2.pdf 11x8, file2.pdf 8x11, incorrect different
    page orientation, file1.pdf is landscape, file2.pdf is portrait.

- Per pixel comparison is done at 8-bit color values.


DEPENDENCIES
------------

Located in the "required" folder.

ImageMagick-7.0.5-5-portable-Q16-x86 (32 bit)
  - compare.exe
    - colors.xml
    - delegates.xml
    - magic.xml
  - convert.exe
    - type.xml

Ghostscript 9.20 for Windows (32 bit)
  - gswin32c.exe
    - gsdll32.dll


CONTACT
-------

Lukas W. DiBeneditto <lukas@dibeneditto.com>
http://dibeneditto.com/
http://github.com/dibeneditto/cadcompare/


