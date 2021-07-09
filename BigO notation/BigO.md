# BigO Notation

## Time Complexity

![1omv0tmikzeaj24z8ps2](https://user-images.githubusercontent.com/70666023/124151018-7625a580-dad5-11eb-8f13-bfe0495df534.jpeg)

A lot of people get confused while understanding the concept of time-complexity, but in this article, we will explain it with a very simple example:

Imagine a classroom of 100 students in which you gave your pen to one person. Now, you want that pen. Here are some ways to find the pen and what the O order is.

### O(n2): 
You go and ask the first person of the class, if he has the pen. Also, you ask this person about other 99 people in the classroom if they have that pen and so on, 
This is what we call O(n2). 

### O(n): 
Going and asking each student individually is O(N). 

### O(log n):
Now I divide the class into two groups, then ask: “Is it on the left side, or the right side of the classroom?” Then I take that group and divide it into two and ask again, and so on. Repeat the process till you are left with one student who has your pen. This is what you mean by O(log n). 

I might need to do the O(n2) search if only one student knows on which student the pen is hidden. I’d use the O(n) if one student had the pen and only they knew it. I’d use the O(log n) search if all the students knew, but would only tell me if I guessed the right side. 

NOTE : We are interested in rate of growth of time with respect to the inputs taken during the program execution .

Another Example:
Time Complexity of algorithm/code is not equal to the actual time required to execute a particular code but the number of times a statement executes. We can prove this by using time command. For example, Write code in C/C++ or any other language to find maximum between N numbers, where N varies from 10, 100, 1000, 10000. And compile that code on Linux based operating system (Fedora or Ubuntu) with below command: 

        gcc program.c – o program
        run it with time ./program

You will get surprising results i.e. for N = 10 you may get 0.5ms time and for N = 10, 000 you may get 0.2 ms time. Also, you will get different timings on the different machine. So, we can say that actual time requires to execute code is machine dependent (whether you are using pentium1 or pentiun5) and also it considers network load if your machine is in LAN/WAN. Even you will not get the same timings on the same machine for the same code, the reason behind that the current network load. 
Now, the question arises if time complexity is not the actual time require executing the code then what is it? 

The answer is : Instead of measuring actual time required in executing each statement in the code, we consider how many times each statement execute. 
For example: 

        int main()
        {
         printf("Hello World");
        }
  
 In above code “Hello World!!!” print only once on a screen. So, time complexity is constant: O(1) i.e. every time constant amount of time require to execute code, no matter which operating system or which machine configurations you are using. 

Now consider another code: 

        void main()
          {
             int i, n = 8;
             for (i = 1; i <= n; i++) {
                 printf("Hello Word !!!\n");
              }
          }

 In above code “Hello World!!!” will print N times. So, time complexity of above code is O(N).
 
                                 Tsum=1 + 2 * (n+1) + 2 * n + 1 = 4n + 4 =C1 * n + C2 = O(n)

### 3.Sum of all elements of a matrix :

For this one the complexity is a polynomial equation (quadratic equation for a square matrix) 
Matrix nxn => Tsum= an2 +bn + c
For this Tsum if in order of n2 = O(n2)
The above codes do not run in the IDE as they are pseudo-codes and do not resemble any programming language . 
So from the above, we can conclude that the time of execution increases with the type of operations we make using the inputs.
The above O -> is called Big – Oh which is an asymptotic notation. There are other asymptotic notations like theta and Ohm.

### How to Compare Algorithms?

To compare algorithms, let us define a few objective measures:

Execution times: Not a good measure as execution times are specific to a particular computer.
A number of statements executed: Not a good measure, since the number of statements varies with the programming language as well as the style of the individual programmer.
Ideal solution:  Let us assume that we express the running time of a given algorithm as a function of the input size n (i.e., f(n)) and compare these different functions corresponding to running times. This kind of comparison is independent of machine time, programming style, etc.

## Resources

* https://www.youtube.com/watch?v=v1SYihb4rcw&t=553s
* https://www.youtube.com/watch?v=Q_1M2JaijjQ
* https://www.bigocheatsheet.com/

## Practice and Exercises

* Cracking The Coding Interview Book
