# Testing/Debugging
---
## Lab 2 Report - January 28, 2022
---
<br/>

# Code Change #1 <br/>
The bug was that if given any link (in this example the failure inducing input contains both image and url links), the program will not check what type of link it is and print it out regardless, which is the symptom. The program should only be printing out website links and not image links so I added an if condition to the while loop to check if there is a "!" before the open bracket. If there is, then it is an image and we do not include it in the output.

![Image](codechange1.png)

Failure-inducing input: [myTest.md](myTest.md)

Symptom: "image.jpg" should not be included in output
![Image](codeChange1Symptom.png)


---
# Code Change #2 <br/>
The bug was that a closing bracket followed by a bunch of text followed by opening parentheses are incorrectly recognized as a link. The failure inducing input included text inbetween the closing bracket and opening parenthses and led to the symptom of the link still being printed out. I fixed this by checking if the next open parentheses directly follows the closing bracket. 


![Image](codeChange2.png)

Failure-inducing input: [test2.md](test2.md)

Symptom: input is not a correctly formatted link so there should be no output
![Image](codeChange2Symptom.png)



---
# Code Change #3 <br/>
The bug was that the program kept searching for the closing link patterns. The failure inducing input of test files that contained the beginnings of link patterns only (like having "(" or "[") caused a symptom of an infinite loop. I fixed this by adding checks to see if closing link components were found. If not, the while loop is exited and there is no longer an infinte loop. 


![Image](codeChange3.png)

Failure-inducing input: [test8-file.md](test8-file.md)

Symptom: infinite loop occurs because the program was searching for the closing link component of either ")" or "]". 
![Image](codeChange3Symptom.png)


