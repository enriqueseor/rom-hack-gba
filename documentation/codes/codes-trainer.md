0 - won't use moves that have no or a negative effect
1 - will actually create some difference in viability scores based on basic calculations
2 - starts understanding things like type effectiveness, damage and fainting
3 - with a chance of about 3/10, some status moves will get priority on the first turn (list of move scripts at 081DBAA7)
4 - with a chance of about 5/10, move effects in this list will get priority: http://pastebin.com/raw.php?i=TP5gCBHp
5 - with a chance of about 4/10, non-damaging moves will get priority
6 - if there are other pokes left on the ai's team, with a chance of a bit more than 6/10 it will give priority to non-damaging moves. chance raises to a bit more than 9/10 if the user (possibly also its ally) has baton pass
7 - 0, 1 and 2 all in one
8 - AI will start looking at health percentages and decide using moves based on that
9 - broken/unfinished, does nothing
10 through 28 - nop
29 - roamer; will attempt to flee on the first turn
30 - safari
31 - unused; will flee on 20% health and lower
