**To MOVE things**

*------------------------*
 NPC MOVE AND TALK
*------------------------*
```
#dynamic 0x800000

#org @start
lock
applymovement 0x0 @movement
waitmovement 0x0
msgbox @talk 0x6
release
end

#org @talk
= I've finished movement!

#org @movement
#raw 0x12
#raw 0x13
#raw 0x13
#raw 0x12
#raw 0x0
#raw 0xFE
```

*------------------*
 MOVE CAMERA
*------------------*
```
#dynamic 0x800000

#org @start
lock
special 0x113
applymovement 0x7F @moveCameraUp
waitmovement 0x0
applymovement 0xFF @movePlayer
waitmovement 0x0
applymovement 0x7F @moveCameraDown
waitmovement 0x0
special 0x114
release
end

#org @moveCameraDown
#raw 0x10
#raw 0x10
#raw 0xFE

#org @movePlayer
#raw 0x12
#raw 0x13
#raw 0x1
#raw 0xFE

#org @moveCameraUp
#raw 0x11
#raw 0x11
#raw 0xFE
```
*-------------------*
 NPC WALK AWAY
*-------------------*
```
#dynamic 0x800000

#org @start
lock
pause 0x60
msgbox @talk1 0x4
closeonkeypressed
pause 0x60
applymovement 0x9 @noticeplayer
waitmovement 0x0
msgbox @talk2 0x6
applymovement 0x9 @disappearNPC
waitmovement 0x0
hidesprite 0x9
setflag 0x200
release
end

#org @disappearNPC
#raw 0xA
#raw 0xA
#raw 0xA
#raw 0xA
#raw 0x9
#raw 0x9
#raw 0x9
#raw 0x9
#raw 0x9
#raw 0x9
#raw 0x9
#raw 0xFE

#org @noticeplayer
#raw 0x0
#raw 0x56
#raw 0x14
#raw 0x14
#raw 0xFE

#org @talk2
= I'm on a secret mission.

#org @talk1
= [grey_fr]... ... ... ... ...
```