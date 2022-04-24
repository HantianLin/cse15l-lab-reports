# CSE15L Lab Report 2 Week 4
Hantian Lin A16923770

---
## First code change
* Code diff:
![change3](change3.png)
* * [Link to the failure-inducing input](https://github.com/HantianLin/markdown-parser/blob/main/new-file.md)
* Symptom of the failure:
![symptom3](symptom3.png)
* The file contains empty lines before. between, and after links. The original code cannot skip these empty lines.\
The symptom is that there is no ouput. The code is trapped in an infinite loop, causing OutOfMemory exception.\
Therefore, there would be no open or close parenthesis to search for, thus the current index would never get updated to escape the while-loop.
However, this did not solve the problem.


---
## Second code change
* Code diff:
![change1](change1.png)
* [Link to the failure-inducing input](https://github.com/HantianLin/markdown-parser/blob/main/new-file.md)
* Symptom of the failure:
![symptom1](symptom1.png)
* I used the same file for testing, same location for empty lines.\
The symptom is that the while-loop is still an infinite loop because the code still cannot resolve empty lines.\
The scanner would not work properly to skip these lines and locate the next parenthesis.


---
## Third code change
* Code diff:
![change2](change2.png)
* [Link to the failure-inducing input](https://github.com/HantianLin/markdown-parser/blob/main/test-file3.md)
* Symptom of the failure:
![symptom2](symptom2.png)
* The file only contains open and close brackets but no open or close parenthesis.\
Therefore, both indexOf methods locating parenthesis would return -1.\
Later in the code, when using the index of open and close parenthesis to coordinate the substring method, the symptom is that the substring method would cause StringIndexOutOfBoundsException since -1 is an invalid index.\
At this point, MarkdownParse passed every test file from lab 3.