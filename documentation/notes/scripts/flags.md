2 states (boolean)
clearflag
setflag

FIRE RED
SAVE FLAGS: 200 - 2FF
SAVE VARS: 0x4011-0x40FF

PERSON ID
NPC Value associated with a flag (not permanent NPC)

*-----------------*
 BASIC FLAG SCRIPT
*-----------------*
```
#dynamic 0x800000

#org @start
lock
faceplayer
checkflag 0x200
if 0x1 goto @alreadyReceived
msgbox @talk1 0x6
giveitem 0xD 0x5 MSG_OBTAIN
setflag 0x200
release
end
```
```
#org @alreadyReceived
msgbox @talk2 0x6
release
end

#org @talk2
= I don't have more Pokéballs!!

#org @talk1
= Here are 5 Pokéballs!!
```
*-------------*
 NPC DISAPPEAR
*-------------*
```
#dynamic 0x800000

#org @start
lock
faceplayer
msgbox @talk 0x6
fadescreen 0x1
hidesprite 0x4
setflag 0x201
fadescreen 0x0
release
end

#org @talk
= I was never here...
```
PERSON ID = 0201

fadescreen
' 0x0 black  --> normal
' 0x1 normal --> black
' 0x2 white  --> normal
' 0x3 normal --> white

----------------------
 NPC NOT ALLOW TO ENTER
------------------------

//SCRIPT EVENT
```
#dynamic 0x800000

#org @start
lock
spriteface 0x4 0x3
spriteface 0xFF 0x4
msgbox @talk 0x6
applymovement 0xFF @movement
waitmovement 0x0
release
end

#org @movement
#raw 0x8
#raw 0xFE

#org @talk
= If you want to enter, you must\nfirst speak to me.
```
spriteface VALUESPRITE DIRECTION
' 0x1 --> down
' 0x2 --> up
' 0x3 --> left
' 0x4 --> right

'0x4 SPRITE ID
'0xFF PLAYER SPRITE

//PERSON EVENT
```
#dynamic 0x800000

#org @start
lock
faceplayer
msgbox @allowPass 0x6
setvar 0x4011 0x1
release
end

#org @allowPass
= You may now enter the building.
```
*--------------*
 CHOOSE STARTER
*--------------*

//PROFESSOR SCRIPT
```
#dynamic 0x800000

#org @start
lock
faceplayer
checkflag 0x200
if 0x1 goto @done
checkflag 0x201
if 0x1 goto @done
checkflag 0x202
if 0x1 goto @done
msgbox @talk1 0x6
spriteface 0x6 0x1
release
end

#org @done
msgbox @talk2 0x6
release
end

#org @talk2
= [blue_fr]Prof[black_fr]: Good choice!

#org @talk1
= [blue_fr]Prof[black_fr]: Choose a starter, [player]!
```

//POKEBALLS SCRIPT

'0xA 0x3 Pokemon middle screen
'0x30 1 seg aprox
'Pokeball  = picture no 92
'Professor = picture no 71
```
#dynamic 0x800000

#org @start
lock
faceplayer
checkflag 0x200
if 0x1 goto @alreadyChoseAPokemon
checkflag 0x201
if 0x1 goto @alreadyChoseAPokemon
checkflag 0x202
if 0x1 goto @alreadyChoseAPokemon
showpokepic 0x01 0xA 0x3
pause 0x30
msgbox @talk1 0x5
compare LASTRESULT 0x1
if 0x1 goto @yes
hidepokepic
release
end

#org @yes
hidepokepic
givepokemon 0x01 0x5 0x0 0x0 0x0 0x0
hidesprite 0x3
setflag 0x200
setflag 0x828
release
end

#org @alreadyChoseAPokemon
msgbox @talk2 0x6
release
end

#org @talk2
= [black_fr]You can not take another!

#org @talk1
= [black_fr]Choose[green_fr] BULBASAUR[black_fr]?
```