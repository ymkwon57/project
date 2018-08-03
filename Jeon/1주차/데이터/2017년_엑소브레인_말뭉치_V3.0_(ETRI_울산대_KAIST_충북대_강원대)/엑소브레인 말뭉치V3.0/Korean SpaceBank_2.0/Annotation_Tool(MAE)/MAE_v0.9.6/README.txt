README.txt, Updated May 10, 2012 for MAE version 0.9.6

License:
  
MAE is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.


Updates from MAE v0.9.5:
  
- This version fixes two bugs:
  - first, if a user sorts the items in a table 
based on the information in a column and then selects and deletes a row, the 
correct row is now deleted
  - second, functionality to scroll to the location of a word in the text window 
has been re-added after it was deleted in a previous version

Updates from MAE v0.9.1:

- Double-clicking the id number of a link tag will highlight both extents involved in the 
link (the extents associated with the FromID and ToID)

- There is a new option in the display menu that allows users to bold and italicize the 
extents associated with each of the different link types.  This will help users to 
more easily see what tagged exents have been linked.  NOTE: the bolding and italicizing 
do not update dynamically at this time--if links are added, the option will have to be 
turned of and then on again in order to see the correct display.



Updates from MAE v0.9:

- Double-clicking on the ID number of an extent tag in the table will highlight the extent in 
the text and move the cursor to that position, as well as highlight any other tags in the 
table that involve that extent.

- The file loading system has been redesigned so that it will be much faster to load texts, unless 
they are very heavily annotated

- A minor bug caused some versions of Windows to add an extra line to the text of the document when saving;
this should be fixed now

- if a DTD contains over 20 tags, the table display will switch to one where the tabs are navigated with 
arrow buttons rather than having all tabs visible at once.


Updates from MAE v0.8.4:

- DTDs can now specify default values for attributes

- It is no longer necessary to have <TEXT></TEXT> tags surrounding files that 
have not previously been annotated--now you can load a file containing only 
text, and the entire contents of the file will be made available for 
annotation.  If you only want to make a portion of a file available for 
annotating, however, you may still use files with <TEXT></TEXT> tags.

- XML output files are now well-formed, and information about encoding 
has been added to the top of the file. Files output by MAE can now be loaded 
into XML parsers such as Python's ElementTree without raising errors.

   NOTE: In order to make files from versions of MAE before 0.9 compliant with XML parsers, 
the offsets of all the tags had to be shifted up by 1 in order to account for the newline
at the end of the line containing the <TEXT> tag.  This means that annotation 
files created by versions of MAE prior to version 0.9 will be off by 1 unless
fixed.  A Python script to make the required adjustments to the files has 
been provided in this package (fix_xml.py).
