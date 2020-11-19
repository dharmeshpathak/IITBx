Below is a code for some routine named function:
Input: Head to the Linked List
print is a function which prints the value to the console
Now answer what does the function print?

```cpp
void function(ListNode *head)
{
  if(head == NULL)
    return;
   
  function(head->next);
  print(head->data);
}
```

Prints all nodes of linked list in reverse order correct
