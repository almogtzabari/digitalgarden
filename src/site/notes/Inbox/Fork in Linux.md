---
{"dg-publish":true,"permalink":"/inbox/fork-in-linux/","tags":[null]}
---



# Fork in Linux
In [[Notes/Linux\|Linux]], fork is a [[System Call\|System Call]] (provided by the [[Notes/Operating System\|OS]]) where a parent (current) [[Inbox/Process\|Process]] is duplicated, along with its registers, memory, Program Counter, etc., in order to create a new [[Inbox/Process\|Process]].

```c
int main(){
	int pid = fork();
	// Q: What is the value of 'pid'?
	// A: For parent pid==PID(child), for child pid==0

	if (pid < 0){
		// Fork failed - handle error
		...
	}
	if (pid > 0){
		// This is the parent process - do parent's code
		...
	}
	else {
		// This is the child process - do child's code
		execv("child_prog", argv_child)
	}
}
```