Let Q1 be a queue containing 6 integers and Q2 be an empty queue. Assume that Front(Q) returns the element at the head/front of the queue Q without removing it from Q. Assume that the function delete of Q deletes the front element from Q and function insert of Q inserts the element into Q.


Consider the following pseduo code:

```cpp

while Q1 is not empty do
          if Front(Q2) <= Front(Q1)  OR  Q2 is empty  then
              x = Front(Q1)
              delete(Q1)
              insert(Q2, x)
          else
              x = Front(Q2)
              delete(Q2)
              insert(Q1, x)
          end if
      end while
  
```  
  
What are the number of iterations of the while loop in the given program if Q1 is [1, 5, 2, 4, 6, 3](Leftmost element is at the top/front of queue)). Enter the answer below:

Answer :- 6

Explanation

iteration 0:
Q1 : [1, 5, 2, 4, 6, 3]
Q2 : []

iteration 1:
Q1 : [5, 2, 4, 6, 3]
Q2 : [1]

iteration 2:
Q1 : [2, 4, 6, 3]
Q2 : [1, 5]

iteration 3:
Q1 : [4, 6, 3]
Q2 : [1, 5, 2]

iteration 4:
Q1 : [6, 3]
Q2 : [1, 5, 2, 4]

iteration 5:
Q1 : [3]
Q2 : [1, 5, 2, 4, 6]

iteration 6:
Q1 : []
Q2 : [1, 5, 2, 4, 6, 3]
