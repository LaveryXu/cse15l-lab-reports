# Researching the `find` Command
1. `find <directory-to-search-in>... -type <descriptor> # searches for files of type <descriptor>`
   - `-type` option enables searching for files of certain type(s)
   - 2 examples: 
      ```
      Jun Xu@DESKTOP-6V69VHU MINGW64 ~/Desktop/Spring 2023/CSE 15L/labs/lab 4/docsearch (main)
      $ find technical -type d # example #1 The descriptor d stands for directory.
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
      $ find technical/ -type f > files-in-technical.txt # example #2 The descriptor f stands for file.

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
   - One case in which `-iname` option is helpful is that when a person makes potential typo(s) of capitalizing some letter(s) in a file's name, performing a case insensitive search helps to see if that file with a potentially mispelled file name exists in <directory-to-search-in>.
   - 2 examples:
      ```
      Jun Xu@DESKTOP-6V69VHU MINGW64 ~/Desktop/Spring 2023/CSE 15L/labs/lab 4/docsearch (main)
      $ find technical/911report/ -name "CHAPTER*.txt" # example #1 That this command line outputs nothing to the terminal indicates that there's no file/directory under technical/911report/, which has the name that matches the pattern "CHAPTER*.txt"

      Jun Xu@DESKTOP-6V69VHU MINGW64 ~/Desktop/Spring 2023/CSE 15L/labs/lab 4/docsearch (main)
      $ find technical/911report/ -iname "CHAPTER*.txt" # example #1
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
      $ find technical/plos -name "jOUrnal*.txt" # example #2 That this command line outputs nothing to the terminal indicates that there's no file/directory under technical/plos, which has the name that matches the pattern "jOUrnal*.txt"

      $ find technical/plos -iname "jOUrnal*.txt" | head # example #2
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

      ```
3. `find <directory-to-search-in>... -empty # searchs for empty files and directories`
   - It's common for someone to want to target empty files and directories in order to delete them.
   - 2 examples:
      ```
      Jun Xu@DESKTOP-6V69VHU MINGW64 ~/Desktop/Spring 2023/CSE 15L/labs/lab 4/docsearch (main)
      $ find technical/ -empty # example #1
      
      ```
      ```
      Jun Xu@DESKTOP-6V69VHU MINGW64 ~/Desktop/Spring 2023/CSE 15L/labs/lab 4/docsearch (main)
      $ find technical/plos -empty # example #2
      
      ```
   - *Note: both uses of `-empty` outputs nothing to the terminal because there's no empty file/directory in technical/*
4. `find <directory-to-search-in>... -size <sizes-range-indicator># searches for files of, less than, or greater than a size or within a size range`
   - `-size` option helps find files of certain sizes or withint certain size ranges
   - 2 examples:
      ```
      $ find technical/ -size +100k # example #1 +100k means greater than 100 kilobytes.
      technical/911report/chapter-1.txt
      technical/911report/chapter-12.txt
      technical/911report/chapter-13.2.txt
      technical/911report/chapter-13.3.txt
      technical/911report/chapter-13.4.txt
      technical/911report/chapter-13.5.txt
      technical/911report/chapter-3.txt
      technical/911report/chapter-6.txt
      technical/911report/chapter-7.txt
      technical/911report/chapter-9.txt
      technical/biomed/1471-2105-3-2.txt
      technical/government/About_LSC/commission_report.txt
      technical/government/About_LSC/State_Planning_Report.txt
      technical/government/Env_Prot_Agen/bill.txt
      technical/government/Env_Prot_Agen/ctm4-10.txt
      technical/government/Env_Prot_Agen/multi102902.txt
      technical/government/Env_Prot_Agen/tech_adden.txt
      technical/government/Gen_Account_Office/ai9868.txt
      technical/government/Gen_Account_Office/d01376g.txt
      technical/government/Gen_Account_Office/d01591sp.txt
      technical/government/Gen_Account_Office/d0269g.txt
      technical/government/Gen_Account_Office/d02701.txt
      technical/government/Gen_Account_Office/gg96118.txt
      technical/government/Gen_Account_Office/GovernmentAuditingStandards_yb2002ed.txt
      technical/government/Gen_Account_Office/im814.txt
      technical/government/Gen_Account_Office/May1998_ai98068.txt
      technical/government/Gen_Account_Office/pe1019.txt
      technical/government/Gen_Account_Office/Sept27-2002_d02966.txt
      technical/government/Gen_Account_Office/Statements_Feb28-1997_volume.txt
      
      ```
      ```
      $ find technical/911report/ -size -100k # example #2 -100k means less than 100 kilobytes.
      technical/911report/
      technical/911report/chapter-10.txt
      technical/911report/chapter-11.txt
      technical/911report/chapter-13.1.txt
      technical/911report/chapter-2.txt
      technical/911report/chapter-5.txt
      technical/911report/chapter-8.txt
      technical/911report/preface.txt

      ```
5. `find <directory-to-search-in>... -newer <file> # searches for files that were modified/created after <file>`
   - helps to find the latest files in <directory-to-search-in>.
   - 2 examples:
      ```
      Jun Xu@DESKTOP-6V69VHU MINGW64 ~/Desktop/Spring 2023/CSE 15L/labs/lab 4/docsearch (main)
      $ find technical/911report/ -newer technical/911report/chapter-5.txt # example 1
      technical/911report/
      technical/911report/chapter-7.txt
      technical/911report/chapter-8.txt
      technical/911report/chapter-9.txt
      technical/911report/preface.txt

      ```
      ```
      $ find technical/government/ -newer technical/government/Alcohol_Problems | head
      technical/government/
      technical/government/Env_Prot_Agen
      technical/government/Env_Prot_Agen/bill.txt
      technical/government/Env_Prot_Agen/ctf1-6.txt
      technical/government/Env_Prot_Agen/ctf7-10.txt
      technical/government/Env_Prot_Agen/ctm4-10.txt
      technical/government/Env_Prot_Agen/final.txt
      technical/government/Env_Prot_Agen/jeffordslieberm.txt
      technical/government/Env_Prot_Agen/multi102902.txt
      technical/government/Env_Prot_Agen/nov1.txt
      ```
I researched options 1,2,4, and 5 on this [Linuxize webpage](https://linuxize.com/post/how-to-find-files-in-linux-using-the-command-line/#find-files-by-type) and researched option 3 on this [GeeksforGeeks webpage](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/).
