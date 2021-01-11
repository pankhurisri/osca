# osca
Problem Statement: Write a C program using fork() system call that generates this sequence in the child process. The starting number will be provided from the user. For example, if 8 is passed as a parameter on the command line, the child process will output 8, 4, 2, 1. Because the parent and child processes have their own copies of the data, it will be necessary for the child to output the sequence. Have the parent invoke the wait() call to wait for the child process to complete before exiting the program. Perform necessary error checking to ensure that a positive integer is passed on the command line. 

Explanation: There is concept named Collatz Conjecture which is concerned with what happens when we take any positive integer n and apply follows the following algorithm:
If n is even, n=(n/2)
Else, n=3*n +1
And this 2 steps are repeated until n=1 is achieved.
In this question, the starting value of n will be provided by the user from command line and parent will invoke wait() function to wait for the child complete the process before exiting the program. 
Algorithm:
1.Write welcome to c.c by pankhuri srivastava
2.Set m=0
3.Declare a vairable that returns the id.
4.Do
A)Write please enter a number greater than 0 to run c.c.
B)Take the input from the user 
While m<=0
5.Call fork function
6.if pid =0, then write child is working.
A)Write the value entered by the user.
B)While m is not equal to 1
I)If m%2=0 then m=m/2;
II)Else, m=m*3+1;
C)write the value of updated m
7.Else, write parent is processing
A)Call wait() function
B)Write parent process is done.
8.Return 0.
 
Description (purpose of use): 
4. one of the major contraint that must be checked is that if the value of n that is passed on the command line is a positive integer. Attach the code snippet of the 
implemented constraint. 
 
Description:
The number that is entered from comand line must be greater than zero 
Test cases: if m=35, then the sequence is:
 35,106,53, 160, 80, 40, 20, 10, 5, 16, 8, 4, 2, 1.

If m=32, then the sequence is:
