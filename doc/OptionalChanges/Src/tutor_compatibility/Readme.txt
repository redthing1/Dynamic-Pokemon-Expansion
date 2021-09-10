How to edit the Tutor Compatibility Tables.

DPE implements an incredibly simple system- no need for painstaking manual edits!
Before we get into how to add the actual entries, we must first account for setup.

Firstly, go to Src/defines.h
In this file, change #define NUM_MOVE_TUTOR_MOVES 128 to how many move tutors you want.
DPE and CFRU add 8 additional move tutors (Total 136) that are not represented in that 128 number.
Do not include them in your new number total.

Secondly, ensure that you customize the move tutors you desire in the following:
Include/tutor.h
Src/TM_Tutor_Tables.c

Ensure that the entries in tutor.h have their names spaced out.
Ensure that TM_Tutor_Tables.c has defines that match the moves as written in Include/moves.h
Ensure that those two files match.

Now you are ready to edit the actual files in the Src/tutor_compatibility/ folder!
Do not define those 8 additional move tutors in this folder either.

Step 1. Name the files like this: # - Move Name

Example:
1 - Mega Punch
2 - Swords Dance
3 - Mega Kick
etc.

Mind the spacing! It will fail to compile if you mess up the syntax!

Step 2. Open the text file. The very first line should read: Tutor #: Move Name

Example:
Tutor 1: Mega Punch

Step 3. Look up the move on Bulbapedia, PokemonDB, Serebii, etc.
Whatever has a move index that lists what pokemon can learn a certain move. My personal preference is Bulbapedia.

Enter the names you see, or customize your own. The names MUST MATCH what their defines are in Include/species.h
They do not necessarily have to be in order, but its best to keep them as such.
If the name is included in the file, it should be inserted in the right place- but better safe than sorry.

Example for file 1:

Tutor 1: Mega Punch
CHARMANDER
CHARMELEON
CHARIZARD
...
PIKACHU
RAICHU
RAICHU_A 