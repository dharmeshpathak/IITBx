sort(it1, it2)[1] is used to sort elements between two pointers(it1 and it2).
std::reverse_iterator [2]produces a new iterator that moves from the end to the beginning of the sequence. 
And min_element(it1, it2) returns iterator of the smallest element in the given range.

Now consider the following blocks of code.

```cpp

    double arr[] = [92, 80, 22, 15, 6, 6, 77, 23, 10, 40, 40];
    vector<double> vec (arr, arr + sizeof(arr) / sizeof(arr[0]));
    vector<double> vec2(vec);
   
    vector<double>::iterator min_vec = min_element(vec.begin(), vec.end());
    sort(vec.begin(),min_vec);
    sort(min_vec, vec.end(), greater<double>());
    
```
   
What is the value of *min_vec?

77
  correct 
  
```cpp  

    vector<double>::reverse_iterator min_vec2 = min_element(vec2.rbegin(), vec2.rend());
    sort(min_vec2, vec2.rend(), greater<double>());
    sort(vec2.rbegin(),min_vec2);
    
```
  
What is the value of vec2[3]?

22
  correct 
