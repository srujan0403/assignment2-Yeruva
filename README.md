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

# Josephus Problem

>In computer science and mathematics, the Josephus Problem (or Josephus permutation) is a theoretical problem. Following is the problem statement: There are n people standing in a circle waiting to be executed. ... The task is to choose the place in the initial circle so that you are the last one remaining and so survive. 

More Details https://www.geeksforgeeks.org/josephus-problem-set-1-a-on-solution

Implementation recursive implementation :
        
        int josephus(int n, int k) {
        return n > 1 ? (josephus(n-1, k) + k - 1) % n + 1 : 1;
        }
        
Non-recursive form :
        
        int josephus(int n, int k) {
        int res = 0;
        for (int i = 1; i <= n; ++i)
        res = (res + k) % i;
        return res + 1;
        }
        
Implementation (for convenience in 0-indexing):

        int josephus(int n, int k) {
        if (n == 1)
        return 0;
        if (k == 1)
        return n-1;
        if (k > n)
        return (josephus(n-1, k) + k) % n;
        int cnt = n / k;
        int res = josephus(n - cnt, k);
        res -= n % k;
        if (res < 0)
        res += n;
        else
        res += res / (k - 1);
        return res;
        }
        
For more details: https://cp-algorithms.com/others/josephus_problem.html
