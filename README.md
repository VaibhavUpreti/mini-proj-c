
# Mini Project Programmin in C

## Contributers-
1. Shivam L1-2
2. Vipul Jain L1-18
3. Mudit Kumar Tyagi L1-22
4. Vaibhav Upreti L1-30


**1. Create a project to demonstrate zombie process.

A zombie or a "defunct process" in Linux(or UNIX based kernel) is a process that has been completed, but its entry still remains in the process table due to lack of
correspondence between the parent and child processes. Usually, a parent process keeps a check on the status of its child processes through the wait() function.
When the child process has finished, the wait function signals the parent to completely exit the process from the memory. However, if the parent fails to call the
wait function for any of its children, the child process remains alive in the system as a dead or zombie process. These zombie processes might accumulate, in large
numbers, on your system and affect its performance.


Below is a c program to creating a Zombie-Process on our system Save this file as zombie.c:

'''
  #include <stdlib.h>
#include <sys/types.h>
#include <unistd.h>

int main ()
{
  pid_t child_pid;

  child_pid = fork ();
  if (child_pid > 0) {
    sleep (60);
  }
  else {
    exit (0);
  }
  return 0;
}

'''


