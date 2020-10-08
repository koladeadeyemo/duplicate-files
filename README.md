# A simple yet powerful program that searches for unique duplicate hashed files on your Windows, mac0S or Linux computer

1. Import os, hashlib, and time modules

2. Create a global my_path variable, which scans all of the directories in the given path and reaches the created file. Then add my_path to the created files in steps 8 and 16

3. Also create a global dictionary of hashed files, a global dictionary of duplicate files, a global ignore list of directories (you can add to this list if you want) and a timer

4. Try to compute and return hash value for given file by opening and reading binary+ file, then computing SHA-1 hash. If file cannot be opened, return false

5. Verify if path contains a directory that is in the ignore_directory_list

6. Split at path (os.sep) will automatically split the path at \ for Windows and / for macOS and Linux

7. Add the .lower() method to convert all directories of path to lowercase and remove empty items ('') associated with the starting and ending points of a path (\ or /)

8. Create a counter and if a file exists, create a separate duplicate_files.txt file which will store all of the duplicate_files

9. Get the complete path of file by looping through and using the walk function in the os module, then join the root and file

10. Find the hash of complete_file_path, and if that hashed_file_path does not exist, skip it

11. If hashed file path is not already in hashed_files_dict, append the complete_file_path (key) and the hashed_file_path (value) to duplicate_files_dict

12. If there are multiple hashed_file_paths (value), assign the complete_file_path (key) to matching_file

13. If the matching file key already exists in duplicate_files_dict, skip it

14. Append matching_file (key) with hashed_file_path (value) to duplicate_files_dict

15. Write to duplicate_files.txt file using the key (complete_file_path) from duplicate_files_dict

16. Create a csv file called 'all_files.csv' and write all of your path files to it (hashed files and duplicate files)

17. Merge the duplicate_files and hashed_files dictionaries

18. Return unique dictionary keys (complete_file_paths) of duplicates

19. Find out how long the program takes to run from start to finish

20. Run program using sudo to run as super-user giving you full administrator privileges, then enter your computer password

Notes:

*Must be running Python 3.6 or above to run this program

*Can be run on Windows, macOS and Linux

*If running via sudo, must use python3, unless you create an alias using the command: alias sudo='sudo '

*Add my_path to both duplicate_files.txt and all_files.csv files to run program from any path
