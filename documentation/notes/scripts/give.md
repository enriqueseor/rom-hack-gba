GIVE POKEMON
```js
#dynamic 0x800000

#org @start
lock
faceplayer
msgbox @talk 0x6
givepokemon 0xPOKEMON 0xLEVEL 0xITEM 0x0 0x0 0x0
release
end

#org @talk
= YOUR TEXT HERE
```
_Before professor gives pokemon givepokemon 0xPOKEMON 0xLEVEL 0xITEM 0x0 0x0 0x0 setflag 0x828_

** GIVE ITEM
```js
#dynamic 0x800000

#org @start
lock
faceplayer
msgbox @talk 0x6
giveitem 0xITEM 0XQUANTITY TYPE_OF_MSG
release
end

#org @talk
= YOUR TEXT HERE
```
_giveitem 0xITEM 0XQUANTITY MSG_OBTAIN_

 **REMOVE ITEM
```js
#dynamic 0x800000

#org @start
lock
faceplayer
msgbox @talk1 0x6
checkitem 0xD 0x1
compare LASTERESULT 0x1
if 0x4 goto @yes
msgbox @talk2
release
end

@org @yes
removeitem 0xD ox1
msgbox @talk3 0x6
release
end

#org @talk3
= [blue_fr]Man[black_fr]: I took a [green_fr]Potion[black_fr]from you!

#org @talk2
= [blue_fr]Man[black_fr]: You don't have what I'm\nlooking for!

#org @talk1
= [blue_fr]Man[black_fr]: Let me check your bag...

'0x0 --> (<)  less than
'0x1 --> (=)  equal to
'0x2 --> (>)  greater than
'0x3 --> (<=) less than or equal to
'0x4 --> (>=) greater than or equal to
'0x5 --> (!=) not equal to
```

 **GIVE POKEMON + 0x5
```js
#dynamic 0x800000

#org @start
lock
faceplayer
msgbox @talk1 0x5
compare LASTRESULT 0x1
if 0x1 goto @abra
msgbox @talk2 0x5
compare LASTRESULT 0x1
if 0x1 goto @machop
msgbox @talk3 0x6
release
end

#org @abra
givepokemon 0x3F 0xF 0x0 0x0 0x0 0x0
goto @complete

#org @machop
givepokemon 0x42 0xF 0x0 0x0 0x0 0x0
goto @complete

#org @complete
msgbox @talk4 0x6
release
end

#org @talk4
= Great choise!

#org @talk3
= How disappointing...

#org @talk2
= How about a machop?

#org @talk1
= Do you want an abra?
```


14F makuhita
151 electrike
