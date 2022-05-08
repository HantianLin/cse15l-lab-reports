# CSE15L Lab Report 3 Week 6
Hantian Lin A16923770

---
## Streamlining ssh Configuration
* My `.ssh/config` file:
![stream1](stream1.png)
I had a hard time manually finding the `.ssh` folder and create the `config` file, so I used terminal instead. I typed the following:
![stream4](stream4.png)
I created and opened the `config` file using terminal and manually typed in the above lines.
* After the `config` file is setted up, I can just type `Han` instead of my full username + hostname, as shown:
![stream3](stream3.png)
* I also used `scp` to copy `RPS.java` to the remote machine using the alias in the terminal, as shown:
![stream5](stream5.png)

---
## Setup Github Access from ieng6
* 

---
## Copy whole directories with `scp -r`
* I used `scp` to cpoy the entire `markdown-parse` directory to the remote machine, as shown:
![scp1](scp1.png)
and by checking using `ls`, the directory is indeed there, as shown:
![scp2](scp2.png)
* After copying, I can compile and run the tests, as shown:
![scp3](scp3.png)