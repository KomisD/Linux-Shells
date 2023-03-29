# Linux-Shells
 Scripts for various works in different linux shells

# Pipe function
This code defines a function named callForks that takes two arguments: an array of integers named inputorder and a character array named filename. The function creates three child processes using the fork() system call. Each child process writes its process ID (PID) and parent process ID (PPID) to a file named filename after waiting for a certain amount of time. The amount of time each child process waits is determined by the value of the corresponding element in the inputorder array. The parent process waits for all three child processes to complete before closing the file.

