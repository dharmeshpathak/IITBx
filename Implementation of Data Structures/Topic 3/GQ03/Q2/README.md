Consider the following code snippet.

```cpp

    queue<int> zebra(queue<int> q){
    stack<int> s;
    queue<int> Q;

    while(!q.empty()){
        s.push(q.front());
        q.pop();
    }

    while(!s.empty()){
        Q.push(s.top());
        s.pop();
    }

    return Q;
}
```  

If the following queue q = [37, 22, 28, 27, 31, 34, 17, 15, 33, 24, 30, 44] is passed to the function zebra, then what element will be at index 5 in the queue returned by the function? Assume that the top of the queue is the leftmost element and indexing starts from 0.

17 correct
