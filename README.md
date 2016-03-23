# Chinook_6_Piece_Endgame_Database

This repository contains a debugged version of the code provided on the Chinook website (https://webdocs.cs.ualberta.ca/~chinook/databases/) that is used to access its 6 piece endgame database.  The code now compiles using the gcc compiler(version 4.8.4).  Exact details on how the database works can be found in the c file itself.

# Major Problems

Although there were only two code breaking errors, it took a considerable amount of time to find them considering that 
I had to figure out how the code worked.

1) Both functions DBrevindex(line 1946) and DBindex(line 1971) where passed references to int arrays but assigned the address to pointers for longs.  Changing the pointers to ints solved this problem.
2) #include <stdlib.h> and #include <stdio.h> needed to be added at the beginning of the program.

The compiler also gave many warnings of lesser importance that were addressed individually.
