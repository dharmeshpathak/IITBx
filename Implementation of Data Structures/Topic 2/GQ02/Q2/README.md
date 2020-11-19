Balanced parentheses means that each opening symbol has a corresponding closing symbol and the pairs of parentheses are properly nested.
For example, consider the following correctly balanced strings of parentheses:
(()()()())
(((())))
(()((())()))
Compare those with the following, which are not balanced:
((((((())
()))
(()()(()
Consider the pseudo-code snippet given below.
    
```cpp

initialize S to be empty stack
while (read next character in input to variable ch)
{
	if( ch == '(' ) {
		push ch onto S
	}
	else if ( ch == ')' and S is non-empty) {
		pop one item of S
	}
	else {
		print "UnBalanced"
		exit the program
	}
}
print "Balanced"

```  
  
Please enter an unbalanced sequence of parenthesis of length atleast 5 below which if fed as input to the pseudo-code above would output "Balanced" .
Please note that the string that you input should have only left parenthesis '(' or right parenthesis ')'. 
The string should not contain any other character like comma or apostrophe or quotes or spaces or tabs etc... except the left parenthesis or right parenthesis. 
The string should have atleast 5 characters.

(((()
        correct 
  
  
  
  
