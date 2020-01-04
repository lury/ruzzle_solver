# Ruzzle Solver
## Introduction: 
Ruzzle is word game played on a 4x4 grid, where the player must attempt to find words to gain the maximum number of points possible in a fixed amount of time. Each letter has a value, and modifiers like double letter and triple word change scores of certain words. This script finds all possible words in a board, and sorts by score. At the bare minimum, the user can provide manual input of the board with or without modifiers like DL and TW, and it will find all words in the board. With pytesseract, the program can use OCR to grab the letters from the board one at a time (this will require some experimentation since we most likely have phone screens with different resolutions). If the user is too lazy to input the words by themselves, this script can also output a list of coordinates for use with AutoInput and Tasker. If the user's android is rooted, adb shell sendevent commands can also be used to autoswipe with better accuracy and speed. These adb shell commands should also work from a computer linked to the phone, and in that case shouldn't require root.
## BARE MINIMUM
If you want the simplest version of this program, in which a 16 letter board is provided and all the top words are found, please use ruzzle_bare_minimum.py. This program requires a file called board.txt in the same directory as the program, and board.txt will contain the letters in the board and information about multipliers (optional). It will write all words sorted by score into a file called words.txt. The 5 prefix files (prefixes2L.txt -> prefixes6L.txt) are required, as well as the dictionary (TWL06.txt). At the bottom of this file, set main_dir to the path to the directory with all the files. Type the board into board.txt, copying the format of the attached example board. The first 4 lines of board.txt should contain the letters of the board, all caps and separated by spaces. Line 5 is blank, and lines 6-9 contain information about multipliers. 2, 3, D, T, and - are DW, TW, DL, TL, and nothing respectively. If you don't want to input multipliers just set all 16 characters to - (scores and word order won't be accurate). There are additional configuration options towards the bottom of the file with explanations.
