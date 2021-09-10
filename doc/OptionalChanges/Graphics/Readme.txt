Refer to the Include/sprite_data.h tutorial file.

If you change the order or add new sprites, make sure the numbers are in order!
Then in the Graphics/frontspr/, Graphics/backspr/, and Graphics/pokeicon/ folders, ensure the inserted sprites match.
They must match the name and number defined in all 5 tables found in Include/sprite_data.h!

Example and Syntax:

01. 	gFrontSprite1101XerneasNaturalTiles[];
02. 	gBackShinySprite1101XerneasNaturalTiles[];
03.	gFrontSprite1101XerneasNaturalPal[];
04.	gBackShinySprite1101XerneasNaturalPal[];
05.	gIconSprite1101XerneasNaturalTiles[];

Simply name the front sprite, back sprite, and icons: 

gFrontSprite1101XerneasNatural.png
gBackShinySprite1101XerneasNatural.png
gIconSprite1101XerneasNatural.png

Make sure every new sprite insert has this.

In Graphics/frontspr/, the image inserted must be a 64x64 FRONT sprite INDEXED to 16 colors with its NORMAL palette.
In Graphics/backspr/, the image inserted must be a 64x64 BACK sprite INDEXED to 16 colors with its SHINY palette.
In Graphics/pokeicon/, the image inserted must be a 32x64 icon sprite for menus and the PC.