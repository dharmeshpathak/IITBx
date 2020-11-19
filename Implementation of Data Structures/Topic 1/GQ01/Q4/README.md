Consider the following block of code

some useful resources on strings

```cpp
using namespace std;
string str("Every cloud has a silver lining");
string result;

//STAGE 1
int str_break1= str.find_first_of(" "); //Note: " " not "", there is a space
int str_break2= str.find_last_of(" ")+1;
str= str.substr(str_break2)+str.substr(str_break1,str_break2-str_break1)+str.substr(0,str_break1);
//End of STAGE 1

//STAGE 2
string::const_iterator cit;   
int index=0;   
for(cit=str.begin(); cit!=str.end(); cit++)
{
  result+=toupper(*cit);
  if (result.at(index)==' '){result[index]='+';}
  index++;
}
// End of STAGE 2   

//STAGE 3
result.replace(11,2,"s6ctw");
//End of STAGE 3

cout <<result.substr(21,5)<<endl;  //Final Result

```

  
What is the output of above code block?

+SILV
  correct 

Explanation

This simple program is to demonstrate some useful inbuilt functions of string class

find_first_of

find_last_of

replace

substr

More details can be found on this PAGE

Initial value of str will be -> Every cloud has a silver lining

At the end of STAGE 1 str will be -> lining cloud has a silver Every

At the end of STAGE 2 str will be -> LINING+CLOUD+HAS+A+SILVER+EVERY

At the end of STAGE 3 str will be -> LINING+CLOUs6ctwHAS+A+SILVER+EVERY

Final Result i.e output of the above block of code is +SILV
