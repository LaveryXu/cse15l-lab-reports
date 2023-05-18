# Researching Commands
For each of those options, give 2 examples of using it on files and directories from ./technical. Show each example as a code block that shows the command and its output, and write a sentence or two about what it’s doing and why it’s useful.

## `find`
1. `find <directory-to-search-in>... -type <descriptor> # searches for files of type <descriptor>`
   - 2 examples: 
      ```
      Jun Xu@DESKTOP-6V69VHU MINGW64 ~/Desktop/Spring 2023/CSE 15L/labs/lab 4/docsearch (main)
      $ find technical -type d # example #1, the descriptor d stands for directory
      technical
      technical/911report
      technical/biomed
      technical/government
      technical/government/About_LSC
      technical/government/Alcohol_Problems
      technical/government/Env_Prot_Agen
      technical/government/Gen_Account_Office
      technical/government/Media
      technical/government/Post_Rate_Comm
      technical/plos
      
      ```
      ```
      Jun Xu@DESKTOP-6V69VHU MINGW64 ~/Desktop/Spring 2023/CSE 15L/labs/lab 4/docsearch (main)
      $ find technical/ -type f > files-in-technical.txt # example #2, the descriptor f stands for file

      Jun Xu@DESKTOP-6V69VHU MINGW64 ~/Desktop/Spring 2023/CSE 15L/labs/lab 4/docsearch (main)
      $ head files-in-technical.txt
      technical/911report/chapter-1.txt
      technical/911report/chapter-10.txt
      technical/911report/chapter-11.txt
      technical/911report/chapter-12.txt
      technical/911report/chapter-13.1.txt
      technical/911report/chapter-13.2.txt
      technical/911report/chapter-13.3.txt
      technical/911report/chapter-13.4.txt
      technical/911report/chapter-13.5.txt
      technical/911report/chapter-2.txt
      
      ```
2. `find <directory-to-search-in>... -iname "<some-string>" # performes a case-insensitive search for files and directories that are named <some-string>`
   - 2 examples:
      ```
      Jun Xu@DESKTOP-6V69VHU MINGW64 ~/Desktop/Spring 2023/CSE 15L/labs/lab 4/docsearch (main)
      $ find technical/911report/ -name "CHAPTER*.txt" # example #1 that this command line outputs nothing to the terminal indicates that there's no file/directory under technical/911report/, which has the name that matches the pattern "CHAPTER*.txt"

      Jun Xu@DESKTOP-6V69VHU MINGW64 ~/Desktop/Spring 2023/CSE 15L/labs/lab 4/docsearch (main)
      $ find technical/911report/ -iname "CHAPTER*.txt"
      technical/911report/chapter-1.txt
      technical/911report/chapter-10.txt
      technical/911report/chapter-11.txt
      technical/911report/chapter-12.txt
      technical/911report/chapter-13.1.txt
      technical/911report/chapter-13.2.txt
      technical/911report/chapter-13.3.txt
      technical/911report/chapter-13.4.txt
      technical/911report/chapter-13.5.txt
      technical/911report/chapter-2.txt
      technical/911report/chapter-3.txt
      technical/911report/chapter-5.txt
      technical/911report/chapter-6.txt
      technical/911report/chapter-7.txt
      technical/911report/chapter-8.txt
      technical/911report/chapter-9.txt

      ```
      ```
      Jun Xu@DESKTOP-6V69VHU MINGW64 ~/Desktop/Spring 2023/CSE 15L/labs/lab 4/docsearch (main)
      $ find technical/plos -name "jOUrnal*.txt" # example #2 that this command line outputs nothing to the terminal indicates that there's no file/directory under technical/plos, which has the name that matches the patter "jOUrnal*.txt"

      Jun Xu@DESKTOP-6V69VHU MINGW64 ~/Desktop/Spring 2023/CSE 15L/labs/lab 4/docsearch (main)
      $ find technical/plos -iname "jOUrnal*.txt"
      technical/plos/journal.pbio.0020001.txt
      technical/plos/journal.pbio.0020010.txt
      technical/plos/journal.pbio.0020012.txt
      technical/plos/journal.pbio.0020013.txt
      technical/plos/journal.pbio.0020019.txt
      technical/plos/journal.pbio.0020028.txt
      technical/plos/journal.pbio.0020035.txt
      technical/plos/journal.pbio.0020040.txt
      technical/plos/journal.pbio.0020042.txt
      technical/plos/journal.pbio.0020043.txt
      technical/plos/journal.pbio.0020046.txt
      technical/plos/journal.pbio.0020047.txt
      technical/plos/journal.pbio.0020052.txt
      technical/plos/journal.pbio.0020053.txt
      technical/plos/journal.pbio.0020054.txt
      technical/plos/journal.pbio.0020063.txt
      technical/plos/journal.pbio.0020064.txt
      technical/plos/journal.pbio.0020067.txt
      technical/plos/journal.pbio.0020068.txt
      technical/plos/journal.pbio.0020071.txt
      technical/plos/journal.pbio.0020073.txt
      technical/plos/journal.pbio.0020100.txt
      technical/plos/journal.pbio.0020101.txt
      technical/plos/journal.pbio.0020105.txt
      technical/plos/journal.pbio.0020112.txt
      technical/plos/journal.pbio.0020113.txt
      technical/plos/journal.pbio.0020116.txt
      technical/plos/journal.pbio.0020121.txt
      technical/plos/journal.pbio.0020125.txt
      technical/plos/journal.pbio.0020127.txt
      technical/plos/journal.pbio.0020133.txt
      technical/plos/journal.pbio.0020140.txt
      technical/plos/journal.pbio.0020145.txt
      technical/plos/journal.pbio.0020146.txt
      technical/plos/journal.pbio.0020147.txt
      technical/plos/journal.pbio.0020148.txt
      technical/plos/journal.pbio.0020150.txt
      technical/plos/journal.pbio.0020156.txt
      technical/plos/journal.pbio.0020161.txt
      technical/plos/journal.pbio.0020164.txt
      technical/plos/journal.pbio.0020169.txt
      technical/plos/journal.pbio.0020172.txt
      technical/plos/journal.pbio.0020183.txt
      technical/plos/journal.pbio.0020187.txt
      technical/plos/journal.pbio.0020190.txt
      technical/plos/journal.pbio.0020206.txt
      technical/plos/journal.pbio.0020213.txt
      technical/plos/journal.pbio.0020214.txt
      technical/plos/journal.pbio.0020215.txt
      technical/plos/journal.pbio.0020216.txt
      technical/plos/journal.pbio.0020223.txt
      technical/plos/journal.pbio.0020224.txt
      technical/plos/journal.pbio.0020228.txt
      technical/plos/journal.pbio.0020232.txt
      technical/plos/journal.pbio.0020241.txt
      technical/plos/journal.pbio.0020262.txt
      technical/plos/journal.pbio.0020263.txt
      technical/plos/journal.pbio.0020267.txt
      technical/plos/journal.pbio.0020272.txt
      technical/plos/journal.pbio.0020276.txt
      technical/plos/journal.pbio.0020297.txt
      technical/plos/journal.pbio.0020302.txt
      technical/plos/journal.pbio.0020306.txt
      technical/plos/journal.pbio.0020307.txt
      technical/plos/journal.pbio.0020310.txt
      technical/plos/journal.pbio.0020311.txt
      technical/plos/journal.pbio.0020337.txt
      technical/plos/journal.pbio.0020346.txt
      technical/plos/journal.pbio.0020347.txt
      technical/plos/journal.pbio.0020348.txt
      technical/plos/journal.pbio.0020350.txt
      technical/plos/journal.pbio.0020353.txt
      technical/plos/journal.pbio.0020354.txt
      technical/plos/journal.pbio.0020394.txt
      technical/plos/journal.pbio.0020400.txt
      technical/plos/journal.pbio.0020401.txt
      technical/plos/journal.pbio.0020404.txt
      technical/plos/journal.pbio.0020406.txt
      technical/plos/journal.pbio.0020419.txt
      technical/plos/journal.pbio.0020420.txt
      technical/plos/journal.pbio.0020430.txt
      technical/plos/journal.pbio.0020431.txt
      technical/plos/journal.pbio.0020439.txt
      technical/plos/journal.pbio.0020440.txt
      technical/plos/journal.pbio.0030021.txt
      technical/plos/journal.pbio.0030024.txt
      technical/plos/journal.pbio.0030032.txt
      technical/plos/journal.pbio.0030050.txt
      technical/plos/journal.pbio.0030051.txt
      technical/plos/journal.pbio.0030056.txt
      technical/plos/journal.pbio.0030062.txt
      technical/plos/journal.pbio.0030065.txt
      technical/plos/journal.pbio.0030076.txt
      technical/plos/journal.pbio.0030094.txt
      technical/plos/journal.pbio.0030097.txt
      technical/plos/journal.pbio.0030102.txt
      technical/plos/journal.pbio.0030105.txt
      technical/plos/journal.pbio.0030127.txt
      technical/plos/journal.pbio.0030129.txt
      technical/plos/journal.pbio.0030131.txt
      technical/plos/journal.pbio.0030136.txt
      technical/plos/journal.pbio.0030137.txt

      ```
3. `find <directory-to-search-in>... -empty # searchs for empty files and directories`
   - 2 examples:
      ```
      Jun Xu@DESKTOP-6V69VHU MINGW64 ~/Desktop/Spring 2023/CSE 15L/labs/lab 4/docsearch (main)
      $ find technical/ -empty
      
      ```
      ```
      Jun Xu@DESKTOP-6V69VHU MINGW64 ~/Desktop/Spring 2023/CSE 15L/labs/lab 4/docsearch (main)
      $ find technical/plos -empty
      
      ```
   - *Note: both uses of `-empty` outputs nothing to the terminal because there's no empty file/directory in technical/*
4. `find <directory-to-search-in>... -size # searches for files of, less than, or greater than a size or within a size range`
   - 2 examples:
5. `find <directory-to-search-in>... -newer <file> # searches for files that were modified/created after <file>`
   - 2 examples:

## `less`
1. less -<>
   1) e.g.
   2) e.g.
2. less -<>
   1) e.g.
   2) e.g.
3. less -<>
   1) e.g.
   2) e.g. 
4. less -<>
   1) e.g.
   2) e.g. 

## `grep`
1. grep -<>
   1) e.g.
   2) e.g.
2. grep -<>
   1) e.g.
   2) e.g.
3. grep -<>
   1) e.g.
   2) e.g.
4. grep -<>
   1) e.g.
   2) e.g.


Along with each option/mode you show, cite your source for how you found out about it as a URL or a description of where you found it.
