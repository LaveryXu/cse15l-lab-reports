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
   1) e.g.
   2) e.g.
5. `find <directory-to-search-in>... -newer <file> # searches for files that were modified/created after <file>`
   1) e.g.
   2) e.g.

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
