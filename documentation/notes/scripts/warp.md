WARP

*------------*
 WARP COMMAND
*------------*

#dynamic 0x800000

#org @start
lock
msgbox @string11 0x6
warp 0xBANK 0xMAP 0xID 0xXPOS 0xYPOS
release
end

#org @string1
= Time to WARP!


'warp
'warphole       'map coodinates correspond to whre the player fell from
'warpmuted      'no sound is played
'warpteleport   'simulates a spin teleport effect
'setwarpcomand  'sets a default warp
