# Comparing MarkdownParse
---
## Lab 5 Report - March 11, 2022
---

# Finding Different Test Results

I stored the outputs of running the tests through each program in a file called `results.txt` in each directory respectively. I used the command:
```
bash script.sh > results.txt
```
I then compared the two result files using the vimdiff command:
```
vimdiff <file1> <file2>
```
I filled in the respective names for the file name and got the result:
![Image](diffTestResults.png) 


# Implementation Differences

## Test 1: 576.md

576.md:
```
![foo *bar*][foobar]

[FOOBAR]: train.jpg "train & tracks"
```

According to the commonmark website output, the expected output should be `[]` because the input is an image so it is not included in the output. 

![Image](576Expected.png)

According to this output, my implementation was correct as it didn't print out any links. The reviewed implementation is incorrect because it prints out a link `train.jpg`.

![Image](576vimdiff.png)

The bug is 




## Test 2: 58.md


![Image](58Expected.png) 

The contents of 576.md:
```
Foo
***
bar
```
![Image](58vimdiff.png)

![Image](.png) 

