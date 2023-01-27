# Processes and signals
![image](https://user-images.githubusercontent.com/105078661/215111354-815d93fc-c398-4b3a-adca-2dddde56c2f9.png)
# Learning Objectives
At the end of this project, you are expected to be able to explain to anyone, without the help of Google:

# General 
- What is a PID
- What is a process
- How to find a process’ PID
- How to kill a process
- What is a signal
- What are the 2 signals that cannot be ignored

# Signals
Signals are (primarily) asynchronous notification of events. There are many different signals which can arise from within or outside the process.
Signals arrive for a process and are posted in the kernel. The kernel can then arrange:
 

- Perform some default action on the process
- To notify the process by causing a signal handler to be invoked in the process. The handler is a user level procedure.

## Where do signals come from

Signals come from either:

A different process: the process invokes a system call which posts a signal to the target process.
The same process: typically, an error such as divide-by-zero.
from the kernel: timer signal (requested by process)
Example:

Signals allow users to control processes. For example, typing the following in csh results:
- ^C in csh causes the shell to send a SIGINT to the current foreground process if any.
- ^Z in csh causes the shell to send a SIGSTOP to the current foreground process.
- typing "fg" sends a SIGCONT signal to the foreground process.

## Signal types:
- termination of a process: death of a child
- process induced exceptions: address violation, floating point error
- unrecoverable errors during a system call: running out of resources such as memory
- unexpected error during a system call: writing a pipe which has no reader, non existant system call, illegal return. Could send an error indication, but programs which don't test error indications would never know.
- emanating from processes in user mode: timer alarm or by sending a signal.
- Terminal interaction: hangup on a login terminal
- Tracing execution of the program.


![image](https://user-images.githubusercontent.com/105078661/215111821-d57e0a9f-44f1-4497-a419-1a9d87b796b5.png)
