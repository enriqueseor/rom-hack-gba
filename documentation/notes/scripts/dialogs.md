### SCAPE CARACTERS

\n = next line (1 time)
\l = next line (x times)
\p = next parragraf

**NPC DIALOG 0x6
```js
#dynamic 0x800000

#org @start
lock
faceplayer
msgbox @talk 0x6
release
end

#org @talk
= YOUR TEXT HERE
```

 **TEXT COLOR
```
#org @talk
= [green_fr]YOUR TEXT HERE

*--------------*
 VARIABLE NAMES
*--------------*

#org @talk
= YOUR TEXT HERE [player]
#org @talk
= YOUR TEXT HERE [rival]
```

 **_MSGBOX ARGUMENTS

0x2 'simple NPC message; no lock, faceplayer or release required
0x3 'signpost script; no lock, faceplayer or release required
0x4 'denotes a stubborn; closeonkeypressed must be used to terminate
0x5 'YES/NO questions;
0x6 'regular message; no special properties

	MSG_FACE = 0x2
	MSG_SIGN = 0x3
	MSG_KEEPOPEN = 0x4
	MSG_YESNO = 0x5
	MSG_NORMAL = 0x6


 **NPC DIALOG 0x2
```js
#dynamic 0x800000

#org @start
msgbox @talk 0x2
end

#org @talk
= YOUR TEXT HERE
```

 **NPC DIALOG 0x4
```js
#dynamic 0x800000

#org @start
lock
faceplayer
msgbox @talk 0x4
closeonkeypressed
release
end

#org @talk
= YOUR TEXT HERE
```

 **MULTICHOICE NPC DIALOG 0x5
```js
#dynamic 0x800000

#org @start
lock
faceplayer
msgbox @talk1 0x5
compare LASTRESULT 0x1
if 0x1 goto @yes
msgbox @talk2 0x6
release
end

#org @yes
msgbox @talk3 0x6
release
end

#org @talk3
= It's my favourite instrument!

#org @talk2
= How unfortunate!

#org @talk1
= [black_fr]Do you play [green_fr]piano[black_fr]
```