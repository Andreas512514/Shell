# Working inside the reverse shell:

1.The first thing to do is use '''bash python3 -c 'import pty;pty.spawn("/bin/bash")'
, which uses Python to spawn a better-featured bash shell. At this point, our shell will look a bit prettier, but we still won’t be able to use tab autocomplete or the arrow keys, and Ctrl + C will still kill the shell.<br>

2.Step two is: **export TERM=xterm** – this will give us access to term commands such as **clear**.<br>

Finally (and most importantly) we will background the shell using **Ctrl + Z**. Back in our own terminal we use **stty raw -echo; fg**. This does two things: first, it turns off our own terminal echo (which gives us access to tab autocompletes, the arrow keys, and **Ctrl + C** to kill processes). It then foregrounds the shell, thus completing the process.<br><br><br>


The full technique can be seen here:

![](https://github.com/Andreas512514/Shell/blob/main/Screenshot%202025-11-27%20170316.png)
