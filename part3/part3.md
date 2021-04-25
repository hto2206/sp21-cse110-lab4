## Part 1
1. The bug was that "result" is calculated as a string instead of a number, meaning for "num1" + "num2", the "+" operator would be a string concatenation instead of a numerical plus. Thus, the result would be "num1num2" string instead of the actual sum.

2. I fixed this by parsing "num1" and "num2" into floats before assigning the (now numerical) sum to result. \
   [Image to the fix](part3-fix.JPG)

## Part 2
3. citylots.json

4. part2.js

5. 11.7MB

6. 3.97s
   
7. Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.85 Safari/537.36

8. Apache

9. Tue, 26 Jan 2021 22:14:13 GMT

10. application/json

11. fetchData()



