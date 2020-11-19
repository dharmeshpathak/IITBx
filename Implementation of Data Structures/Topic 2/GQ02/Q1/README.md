Given postix expression:
a b ^ c d e * + f - * g /

We want to evaluate this postix expression by using the usual stack algorithm discussed in Topic 2 session 14.
What will be the maximum size of the stack at any time during the evaluation given expression for some given values of variables?

4

What is the value of the given postfix expression when a = 4, b = 2, c = 5, d = 6, e = 7, f = 8, g = 3?

208

Which of the following infix expressions correctly captures the given postfix expression?

( ( a ^ b ) * ( c + ( d * e ) - f ) ) / g

Explanation

We know that in the algorithm, we push the operands into the stack and as soon as we encounter a operator, 
we will do the operation corresponding to that operator with the top two elements of stack and push back the value into the stack.
Therefore, in-order to get the maximum size of stack, we first look at that maximum lenght sub-string inside given expression with operands alone. 
And analyze the size of stack just before the substring. This size added to the lenght of substring is nothing but the answer which is 4 in this case.
It is a good idea to first solve the third question and then proceed to second question since evaluating a infix expression is much easier than evaluating a postfix expression by hand.
The infix expression can be obtained by using a small patch over algorithm that stated in class for evaluation.
In this case, when ever we are to evaluate the top two elements of stack with the operation we just make a string with those two operands and operator and push that into stack. 
Thus, after the algorithm, we will be left with infix expression on the top of the stack. It is very easy to solve the evaluation question using this infix expression.
