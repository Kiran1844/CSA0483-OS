# CSA0483-OS

1-> SYSTEM CALL INVOKING:-

   ALGORITHAMIC STEPS:-

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
   
2->COPY THE CONTENT OF ONE FILE TO OTHER:-

  ALGORITHAMIC STEPS:-
  
 1)Include the necessary header files, such as stdio.h, stdlib.h, unistd.h, and fcntl.h.

 2)Define a buffer size (e.g., BUFFER_SIZE) to read and write data in chunks.

 3)Declare variables to store file descriptors for the source and destination files (source_fd and dest_fd), 
   as well as variables to store the number of bytes read and written (bytes_read and bytes_written), and a buffer to hold data.

 4)Open the source file for reading using the open() system call with the O_RDONLY flag. Check for errors in opening the source file.

 5)Open or create the destination file for writing using the open() system call with the O_WRONLY and O_CREAT flags. 
   Specify file permissions (e.g., S_IRUSR | S_IWUSR) to allow reading and writing by the owner. Check for errors in opening/creating the destination file.

 6)Use a loop to read data from the source file in chunks of BUFFER_SIZE bytes using the read() system call. 
 Continue until the end of the source file is reached.Check for errors during reading.

 7)Write the read data to the destination file using the write() system call. Check for errors during writing.

 8)Close both the source and destination files using the close() system call.

 9)Display a success message indicating that the file was copied successfully.
