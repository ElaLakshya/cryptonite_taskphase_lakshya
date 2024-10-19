# Pondering PATH

## Flags

```
### 1. The PATH variable

- [x] pwn.college{E7tCDDgiHRybonA3ZNeXISQbnn9.dZzNwUDL5ITO0czW}

hacker@path~the-path-variable:~$ PATH=""
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{E7tCDDgiHRybonA3ZNeXISQbnn9.dZzNwUDL5ITO0czW}

We had to simply destroy the PATH variable so no directory can be located, thus even rm command can't be found hence /challenge/run can't remove the flag

### 2. Setting PATH

- [x] pwn.college{ob68qcTi00apYyoVa6DB9Nqsy_3.dVzNyUDL5ITO0czW}

hacker@path~setting-path:~$ PATH=/challenge/more_commands
hacker@path~setting-path:~$ /challenge/run win
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{ob68qcTi00apYyoVa6DB9Nqsy_3.dVzNyUDL5ITO0czW}

### 3. Adding Commands

- [x] pwn.college{YBIoXenZ-nOIpBTbE7WAODhrn_-.dZzNyUDL5ITO0czW}

hacker@path~adding-commands:~$ touch win
hacker@path~adding-commands:~$ nano win

The command in nano  was

"read flag < /flag
echo $flag"

hacker@path~adding-commands:~$ chmod ugo=rwx win
hacker@path~adding-commands:~$ PATH=~
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
pwn.college{YBIoXenZ-nOIpBTbE7WAODhrn_-.dZzNyUDL5ITO0czW}

### 4. Hijacking Commands

- [x] pwn.college{4moYsf_m_7MHM0ueJcztddfGt95.ddzNyUDL5ITO0czW}

hacker@path~hijacking-commands:~$ touch rm
hacker@path~hijacking-commands:~$ nano rm
hacker@path~hijacking-commands:~$ chmod o+x rm
hacker@path~hijacking-commands:~$ PATH=~
hacker@path~hijacking-commands:~$ /challenge/run
Trying to remove /flag...
pwn.college{4moYsf_m_7MHM0ueJcztddfGt95.ddzNyUDL5ITO0czW}

In this puzzle we changed the rm command itself! We switched the path of rm to the same as our path command which reads out our flag.

The command used was 

"read flag < /flag
echo $flag"
```

