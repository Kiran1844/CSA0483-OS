# CSA0483-OS

1. System call Invocation

   ALGORITHAMIC STEPS:

 1)Include the necessary header files, such as stdio.h and unistd.h.

 2)Declare two pid_t variables to store the process identifiers for the current process and the child process.

 3)Use the fork() system call to create a new child process.
   The fork() system call will return the child's PID in the parent process and 0 in the child process.
 
 4)Check the return value of fork():
 
 5)If it's less than 0, the fork failed, and you should display an error message and exit.

 6)If it's 0, it means you're in the child process,
   so you can display the child's PID using getpid() and the parent's PID using getppid().

 7)If it's greater than 0, you're in the parent process,
   so you can display the parent's PID using getpid() and the child's PID, which is the value returned by 
   fork().
 
 8)Print the process identifiers and any other information you want to display.
 
 9)End the program.
   
