Consider a child is playing game where he/she places(push) and removes(pop) numbered cubes in an empty stack, from a basket. The basket has 10 uniquely numbered cubes (0-9) and the cube pushed on the stack should be the largest value of the 'cube' in the basket. The cube returns back to the basked when removed(popped) from the stack. As a part of the game, the child performs sequences of push and pop operations.

>>Which of the following pop sequences could not occur in his/her game?

Solution - 9, 2, 5, 6, 4, 3, 3, 2

Explanation for : 7, 8, 9, 6, 6, 7, 6, 7, 8, 9

STACK -> [ ]
Basket: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
After push :[9, 8, 7] After pop :[]
Pop sequences: 7, 8, 9

Basket: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
After push :[9, 8, 7, 6] After pop :[9, 8, 7]
Pop sequences: 7, 8, 9, 6

Basket: 0, 1, 2, 3, 4, 5, 6
After push :[9, 8, 7, 6] After pop :[9, 8]
Pop sequences: 7, 8, 9, 6, 6, 7

Basket: 0, 1, 2, 3, 4, 5, 6, 7
After push :[9, 8, 7, 6] After pop :[]
Pop sequences: 7, 8, 9, 6, 6, 7, 6, 7, 8, 9

Explanation for : 6, 7, 8, 6, 7, 8, 8, 9, 9

STACK -> [ ]
Basket: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
After push :[9, 8, 7, 6] After pop :[9]
Pop sequences: 6, 7, 8

Basket: 0, 1, 2, 3, 4, 5, 6, 7, 8
After push :[9, 8, 7, 6] After pop :[9]
Pop sequences: 6, 7, 8, 6, 7, 8

Basket: 0, 1, 2, 3, 4, 5, 6, 7, 8
After push :[9, 8] After pop :[]
Pop sequences: 6, 7, 8, 6, 7, 8, 8, 9

Basket: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
After push :[9] After pop :[]
Pop sequences: 6, 7, 8, 6, 7, 8, 8, 9, 9

Explanation for : 9, 9, 8, 9, 5

STACK -> [ ]
Basket: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
After push :[9] After pop :[]
Pop sequences: 9

Basket: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
After push :[9] After pop :[]
Pop sequences: 9, 9

Basket: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
After push :[9, 8] After pop :[]
Pop sequences: 9, 9, 8, 9

Basket: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
After push :[9, 8, 7, 6, 5] After pop :[9, 8, 7, 6]
Pop sequences: 9, 9, 8, 9, 5

Explanation for : 9, 2, 5, 6, 4, 3, 3, 2

Follow the operations carefully, you will find some wrong operations or misplaced cubes

STACK -> [ ]
Basket: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
After push :[9] After pop :[]
Pop sequences: 9

Basket: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
Er: After push :[0, 1, 2] After pop :[0, 1]
Pop sequences: 9, 2

Basket: 9, 8, 7, 6, 5, 4, 3, 2
After push :[0, 1, 2, 3, 4, 5, 6] After pop :[0, 1, 2]
Pop sequences: 9, 2, 6, 5, 4, 3

Basket: 9, 8, 7, 6, 5, 4, 3
After push :[0, 1, 2, 3] After pop :[0, 1]
Pop sequences: 9, 2, 6, 5, 4, 3, 3, 2
