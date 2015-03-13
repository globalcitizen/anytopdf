`anytopdf` is a (5+ year abandoned) `perl` script that converts OpenOffice.org, Microsoft Office (Word DOC, Excel XLS), RTF, HTML, and other openoffice.org readable file formats to the PDF format. It will automatically install the supporting 'AnyToPDF' OpenOffice?.org Basic macro library in the current user's OpenOffice?.org configuration if it's not already present.

Important
---------

Many of the OpenOffice?.org developers have moved to a forked project, LibreOffice at http://www.libreoffice.org/

Since this appears to be the future of the OpenOffice.org codebase, testing and modification is required to support using LibreOffice instead of OpenOffice.org as the backend conversion binary.

Volunteers welcome, my time is unfortunately limited at present.

Usage
-----

`anytopdf <input file> <output file.pdf>`


Dependencies
------------
 * Requires OpenOffice.org v3+
 * Unix-style platform
 * `perl`


Thanks
------
 * http://www.togaware.com/linux/survivor/Convert_MS_Word.html / DannyB : original macro code
 * OpenOffice.org users and contributors
 * Unix hackers with a conscience who don't work for morally bankrupt corporations, governments and militaries. 


Notes
-----

 * Not very efficient as it has to start an entire OpenOffice.org instance for each execution
 * Does not support attempts to use file names with commas, brackets, quotes or new lines (due to system() issue: see Contribute section below...) 


Contribute
----------
 * Write a daemon version using some form of IPC with the macro library, so that multiple executions can run against a single OpenOffice?.org instance
 * Fix the `perl` `system()` issue (see source)
 * Adapt to support other (eg: windows) platforms 
