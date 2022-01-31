# assignment2-Yeruva
This repo is for assignment 2
# Srujan Kumar Reddy Yeruva
#### Cafe Bahar would be my favourite place to buy food

The atmosphere is very **happening** and **thriving**
which is what i love about that place

--------------------------------------------------------------------------

# Directions to my favourite food place
###### Rajiv Gandhi international Airport, is the nearest airport


1. Follow the approaching road to NH 44.
2. Take the NH 44 until you reach Masab Tank Flyover
3. Take Lakdikapul road 
4. Follow LB Stadium Rd and Raja Reddy Marg to your destination

### some food items
* Chicken Biryani
* Mutton Biryani
* Basically all kinds of biryanis


[Know more about me](https://github.com/srujan0403/assignment2-Yeruva/blob/main/AboutMe.md)

-----------------------------------------------

# Sports

Cricket, Tennis, Squash and Badminton are the sports i would recommend to try.

|  Name       |  Location   | Amount|
|-------------|-------------|-------|
|  Cricket    | South hall  |  $39  |
|  Tennis     | Outdoor     |  $49  |
|  Squash     | Recreation  |  $8   |
|  Badminton  | Recreation  |  $39  |

----------------------------------------------------

# Quotes

> "Greater Perhaps" - John Green

> "Get busy living or get busy dying" - Stephen King

----------------------------------------------------

# 15 Puzzle Game: Existence Of The Solution

This game is played on a  board. On this board there are  playing tiles numbered from 1 to 15. One cell is left empty (denoted by 0). You need to get the board to the position presented below by repeatedly moving one of the tiles to the free space:

 
 
The game "15 Puzzle” was created by Noyes Chapman in 1880.

Existence Of The Solution
Let's consider this problem: given a position on the board, determine whether a sequence of moves which leads to a solution exists.

Suppose we have some position on the board:

 
 
where one of the elements equals zero and indicates an empty cell 

Let’s consider the permutation:

i.e. the permutation of numbers corresponding to the position on the board without a zero element

Let  be the number of inversions in this permutation (i.e. the number of such elements  and  that , but ).

Suppose  is an index of a row where the empty element is located (i.e. using our convention, ).

Then, the solution exists iff  is even.

Implementation
The algorithm above can be illustrated with the following program code:


int a[16];
for (int i=0; i<16; ++i)
    cin >> a[i];

int inv = 0;
for (int i=0; i<16; ++i)
    if (a[i])
        for (int j=0; j<i; ++j)
            if (a[j] > a[i])
                ++inv;
for (int i=0; i<16; ++i)
    if (a[i] == 0)
        inv += 1 + i / 4;

puts ((inv & 1) ? "No Solution" : "Solution Exists");
Proof
In 1879 Johnson proved that if  is odd, then the solution doesn’t exist, and in the same year Story proved that all positions when  is even have a solution.

However, all these proofs were quite complex.

In 1999 Archer proposed a much simpler proof.
you can download from the link [here](http://www.cs.cmu.edu/afs/cs/academic/class/15859-f01/www/notes/15-puzzle.pdf)
