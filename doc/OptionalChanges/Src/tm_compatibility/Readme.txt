How to edit the TM and HM Compatibility Tables.

DPE implements an incredibly simple system- no need for painstaking manual edits!
Before we get into how to add the actual entries, we must first account for setup.

Firstly, go to Src/defines.h
In this file, change #define NUM_TMSHMS 128 to how many TMs + HMs you want.

Secondly, ensure that you customize the TMs and HMs you desire in the following:
Src/TM_Tutor_Tables.c

Ensure that TM_Tutor_Tables.c has defines that match the moves as written in Include/moves.h!
HMs go last in the table!

Now you are ready to edit the actual files in the Src/tm_compatibility/ folder!

Step 1. Name the files like this: # - Move Name

Example:
1 - Focus Punch
2 - Dragon Claw
3 - Water Pulse
...
121 - Cut
122 - Fly

Mind the spacing! It will fail to compile if you mess up the syntax!

Step 2. Open the text file. The very first line should read: Tutor #: Move Name

Example:
TM01: Focus Punch
TM02: Dragon Claw
...
HM01: Cut
HM02: Fly

Step 3. Look up the move on Bulbapedia, PokemonDB, Serebii, etc.
Whatever has a move index that lists what pokemon can learn a certain move. My personal preference is Bulbapedia.

Enter the names you see, or customize your own. The names MUST MATCH what their defines are in Include/species.h
They do not necessarily have to be in order, but its best to keep them as such.
If the name is included in the file, it should be inserted in the right place- but better safe than sorry.

Example for file 1:

TM01: Focus Punch
CHARMANDER
CHARMELEON
CHARIZARD
SQUIRTLE
WARTORTLE
BLASTOISE
PIKACHU
PIKACHU_SURFING
PIKACHU_FLYING
PIKACHU_COSPLAY
PIKACHU_LIBRE
PIKACHU_POP_STAR
PIKACHU_ROCK_STAR
PIKACHU_BELLE
PIKACHU_PHD
PIKACHU_CAP_ORIGINAL
PIKACHU_CAP_HOENN
PIKACHU_CAP_SINNOH
PIKACHU_CAP_UNOVA
PIKACHU_CAP_KALOS
PIKACHU_CAP_ALOLA
PIKACHU_CAP_PARTNER
RAICHU
RAICHU_A
SANDSHREW
SANDSHREW_A
SANDSLASH
SANDSLASH_A
NIDOQUEEN
NIDOKING
etc.