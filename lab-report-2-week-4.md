# Testing/Debugging
---
## Lab 2 Report - January 28, 2022
---
<br/>

# Code Change #1 <br/>
If given an image link, the program will print that out. But it should only be printing out website links and not image links. Added an if condition to the while loop to check if there is a "!" before the open bracket. If there is, then it is an image and we do not include it in the output.

![Image](codechange1.png)

Failure-inducing input: [myTest.md](myTest.md)

Symptom: "image.jpg" should not be included in output
![Image](codeChange1Symptom.png)


---
# Code Change #2 <br/>
Parentheses followed by a bunch of text followed by brackets are incorrectly recognized as a link. Fixed by checking if the next open bracket directly follows the closing parentheses. 


![Image](codeChange2.png)

Failure-inducing input: [test2.md](test2.md)

Symptom: input is not a correctly formatted link so there should be no output
![Image](codeChange2Symptom.png)



---
# Code Change #3 <br/>
Test files that contained the beginnings of link patterns only (like having "(" or "[") caused an infinite loop. Fixed by adding checks to see if closing link components were found. If not, the while loop is exited and there is no longer an infinte loop. 


![Image](codeChange3.png)

Failure-inducing input: [test8-file.md](test8-file.md)

Symptom: infinite loop occurs because the program was searching for the closing link component of either ")" or "]". 

![Image](codeChange3Symptom.png)


