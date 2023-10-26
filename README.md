# midway-preasm-powershell
An implementation of the preasm tool used by various Midway games in PowerShell.

Run it from a directory containing .asm files, and it will produce some .axx files.
axx files will be cleaned of lines with * ; and #label duplicates will be fixed.

Todo:
- Command line options
- Fix fringe cases like these where we don't want to change the #NXT or others in the struct.

#lp1    move    *a0(#NXT),a14,W 
	STRUCT	0
	WORD	#XPOS
	WORD	#ZPOS
	WORD	#YPOS
	WORD	#INRING
	LABEL	#SIZE
	WORD	#NXT	;first element of NEXT entry. check for -1.

- More exceptions?


