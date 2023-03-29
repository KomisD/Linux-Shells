# Linux-Shells
 Scripts for various works in different linux shells

# Pipe function
This code defines a function named callForks that takes two arguments: an array of integers named inputorder and a character array named filename. The function creates three child processes using the fork() system call. Each child process writes its process ID (PID) and parent process ID (PPID) to a file named filename after waiting for a certain amount of time. The amount of time each child process waits is determined by the value of the corresponding element in the inputorder array. The parent process waits for all three child processes to complete before closing the file.

# Segmentation fault handler
This code defines a function named safeWrite that takes two arguments: a pointer to an integer named ptr and an integer named val. The function attempts to write the value of val to the memory location pointed to by ptr. If ptr is NULL, the function returns 1. If the write operation causes a segmentation fault (SIGSEGV), the function also returns 1. Otherwise, the function returns 0. The function uses the signal() system call to set up a signal handler for SIGSEGV. The signal handler uses sigsetjmp() and siglongjmp() to return control to the point where the signal was raised.

# Signal caller
This code defines a function named sendSignal that takes two arguments: a string named signal and a string named pid. The function checks if the number of arguments passed to it is equal to 2. If not, it prints “Bad usage”. If yes, it sets the value of signal and pid to the first and second elements of the $argv array respectively. The function then uses the kill command to send the signal specified by signal to the process specified by pid. Before sending the signal, the function checks if the signal is valid by using the kill -L command to list all available signals and then using grep to search for the specified signal. If the signal is not valid, the function prints “Signal error”. If the process specified by pid does not exist, the function prints “Process not found”.
