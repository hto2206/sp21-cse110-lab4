## Variables and scoping
### Part 1a:
1. values added:  20
2. final result:  20
3. values added:  20
4. **Error**: result is only accessible within its block scope, but we are calling it from an outside block.
5. **Error**: result is constant, but we are trying to reassign it
6. **Error**: result is constant, so either this line is unreachable due to the error in the previous line, or "result" is undeclared in this scope if the previous error is commented out (since "constant" gives the same scope as "let")

### Part 1b:
1. The code will print "3", which is the number of iterations of the previous for-loop
2. The code will print "150", which is the discountedPrice calculated in the last iteration of the for-loop;
3. The code will print "150", which is the finalPrice calculated in the last iteration of the for-loop;
4. The code will return an array of discounted prices: [50, 100, 150], which in this case is an array where each element is half of the element at the same index of the parameter array "prices".
5. **Error**: "i" is not defined, since "let" here only gives the scope of "i" to be within the for-loop.
6. **Error**: "discountedPrice" is not defined, since "let" here only gives the scope of "discountedPrice" to be within the for-loop.
7. The code will print "150" as in part1b(3), since the scope of "let" here is the whole function. 
8. The code will return [50, 100, 150] normally as in part1b(4), since the scope of "let" here is the whole function. 
9. **Error**: "i" is not defined, since "let" here only gives the scope of "i" to be within the for-loop.
10. The code will print "3", since "length" counts the number of elements in the parameter array "prices".
11. The code will return [50, 100, 150] normally as in part1b(4), since the "const" declaration only stops the array from being reassigned but not its elements. 

## Data Types
12. A. ```student.name```                     \
    B. ```student['Grad Year']```             \
    C. ```student.greeting()```               \
    D. ```student['Favorite Teacher'].name``` \
    E. ```student.courseLoad[0]```        

## Basic operators and Type conversion
13. A. '32'  , because the "+" operator is also used for string concatenation, so once a string is detected, "+" means concatenation. \
    B. 1     , because the "-" operator is not well-defined for strings, so it only refers to numerical subtraction.  \
    C. 3     , because "null" variable can refer to a numerical 0, and no strings is detected so "+" is numerical. \
    D. 3null , because a string is detected, so "+" means concatenation. \
    E. 4     , because "true" variable can refer to a numerical 1, and no strings is detected so "+" is numerical. \
    F. 0     , because both "null" and "false" variable can refer to a numerical 0, and no strings is detected so "+" is numerical. \
    G. 3undefined, because '3' is a string, so "+" means concatenation and so undefined is concatenated as a string to '3'. \
    H. NaN   , because the "-" operator here is numerical, and undefined is not a number, so it returns Not-a-Number. 

14. A. true, since string '2' becomes a number. \
    B. false, since the first character of string '2' is larger than the first character of string '12' (which is '1') in dictionary order.  \
    C. true, since '2' is converted to numbers by the equality operator "==". \ 
    D. false, since '2' is not converted to numbers by the operator "===", and so the types of the operands are different. \
    E. false, since in numerical terms, true equals 1, and 1 does not equal to 2.  \
    F. true, since "Boolean" would return false only if the object's value is omitted or is equal to 0, -0, null, false, NaN, undefined, or the empty string. 

15. "==" means equal, where if the operands are of different types, their values are automatically converted to numbers to compare. On the other hand, "===" means strict equality, so it checks the equality without type conversion (so if operands are of different types, it automatically returns false). 

## Loops
16.  [Code of Question 16](part1b-question16.js)

## Functions
17.   The function will return [2,4,6]. First, a new array newArr is created to be modified and returned. Then, the for-loop iterates through the elements in the parameter array and push new elements into newArr, where these new elements are given by the callback function and the elements of "array" at the current index. Then, since the callback function doubles any number passed in, the elements of newArr will be twice the elements of "array" at the same index. 

18.  [Code of Question 18](part1b-question18.js)

19. The output of the code is:  \
     1  \
     4  \
     3  \
     2  
 This is because "SetTimeout" will call a function after some miliseconds of delay. And a delay of "0" means that it will execute as soon as possible when the execution thread is not busy. So, 1 is invoked first, then 4, then the execution thread is not busy so 3 is called, and 2 is called after a delay of 1 second.
