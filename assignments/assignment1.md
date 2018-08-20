# Code Review Assignments
Code review should be heavily focused on clarity, communication, and collaboration. Any assignments we produce should perhaps be graded more like an essay - tone and content matter more than spotting the logic bugs.

Below are some example assignments.

# Description 

This homework asks you to write code for a code review that we will have in class. The code will be reviewed by your peers in class.
 
The application you will be writing for is intended to run on a small, inexpensive embedded device that does not have a floating point unit. This means that the processor can only do integer arithmetic. However, the device does have a display and needs to display the result of floating point arithmetic to the user. Because this is a small inexpensive processor there is no support for strings or any mathematical library functions. You must write all the code yourselves performing all the floating point math with integers only and no strings! Character arrays, or C strings, can't tell you their size but they do end with a '\0' character. 
 
The requirements for the code are to write the following functions:
 
## Conversion Functions

The two functions, characteristic() and mantissa(), will break a character array into a characteristic and a mantissa. The characteristic for the number 2.351 is 2 and the mantissa is 351 over 1,000. The characteristic for the number 0.0125 is 0 and the mantissa is 125 over 10,000. The characteristic for the number -4.0 is -4 and the mantissa is 0 over 10. These values should be stored in the reference parameters c, numerator and denominator. The C string may include leading or trailing spaces, unary plus or minus signs, integers, or real numbers. Your functions must handle all of these cases. If an invalid string is passed in your function will return false. If the passed in string was valid return true.
 
```
bool characteristic(char numString[], int& c);
bool mantissa(char numString[], int& numerator, int& denominator);
...
...
char number[] = "123.456";
int c, n, d;
 
//if the conversion from C string to integers can take place
if(characteristic(number, c) && mantissa(number, n, d))
{
    //do some math with c, n, and d
}
else
{
    //handle the error on input
}
```
 
## Math Functions
These two functions take as parameters two sets of mantissa and characteristic and a char array to hold the result of the arithmetic operations. The result of the add or subtract should be converted into char's and placed in the result array. The array must end with a '\0'. The 'len' parameter tells how many characters can be placed on the result array. For these functions to return true you must at a minimum store the characteristic of the result. If the result is a non-integer place as many of the digits as will fit in the result after a decimal point. 
 
```
bool add(int c1, int n1, int d1, int c2, int n2, int d2, char result[], int len);
bool subtract(int c1, int n1, int d1, int c2, int n2, int d2, char result[], int len); 
...
...
 
 
char answer[100];
int c1, n1, d1;
int c2, n2, d2;
 
c1 = 1;
n1 = 1;
d1 = 2;
 
c2 = 2;
n2 = 2;
d2 = 3; 
 
//if the C string could hold at least the characteristic
if(add(c1, n1, d1, c2, n2, d2, answer, 100))
{
    //display string with answer 4.166666666...
}
else
{
    //display error message
}
```
 
These two functions take as parameters two sets of mantissa and characteristic and a char array to hold the result of the arithmetic operations. The result of the multiply or divide should be converted into char's and placed in the result array. The 'len' parameter tells how many characters can be placed on the result array. You cannot assume that any of the functions in this assignment will be available to use in your code. Any code that you submit for review cannot contain a call to someone else's code.

```
bool multiply(int c1, int n1, int d1, int c2, int n2, int d2, char result[], int len);
bool divide(int c1, int n1, int d1, int c2, int n2, int d2, char result[], int len);
...
...
char answer[100];
int c1, n1, d1;
int c2, n2, d2;
 
...
...
 
if(divide(c1, n1, d1, c2, n2, d2, answer, 100))
{
    //display string with answer
}
else
{
    //display error message
}
```
 
All the functions return a boolean value indicating the success or failure of the operation. Improper data is the most likely cause for a function to fail. You may add your own additional helper functions (I had at least a half dozen) but you must include them for the review. Do not change the interface to these functions.
 
Each of you will be assigned a function (see below). You must implement your function by Monday the 25th. On Wednesday the 27th we will begin our code reviews (you have a few days to prepare for the review). After the review you will receive a list of items that need to be changed (as decided by the review team), The final part of the assignment is to implement the changes. If you are not present for the review, do not have your code on the 25th to distribute to the other team members, or do not hand in your updated code you will not receive credit for the assignment. 