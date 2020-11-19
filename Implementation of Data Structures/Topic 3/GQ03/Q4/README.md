Consider the pseudo code of the function given below.

```cpp      
void fn1(ListNode *node)
{
  ListNode *p1 = node, *pt2 = node;
  while (p1 != NULL && pt2 != NULL && pt2->next != NULL) {
    	p1 = p1 -> next;
    	pt2 = pt2 -> next -> next;
  }
  print(p1);
}
```
    
What will the above function fn1 print if the head of a linked list is passed as argument to the function? Note: 'print' is a function which prints the value to the console


Node pointer at middle of linked list correct

Explanation

This is one of the methods used to find the center of linked list. p1 is called a slow pointer(iterator) 
since it moves one step at a time and pt2 is called a fast pointer(iterator) since it moves two steps at a time. By the time pt2 reaches end, 
p1 reaches the middle of the linked list. Then the function prints the ptr(not data) of p1.
