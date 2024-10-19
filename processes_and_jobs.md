# Processes and Jobs

## Flags

### 1. Listing Processes

- [x] pwn.college{4a3W90exrJDhudSQk0Zc5EQSBTI.dhzM4QDL5ITO0czW}

hacker@processes~listing-processes:~$ ps aux

USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND

root           1  0.0  0.0   1056   640 ?        Ss   06:34   0:00 /sbin/docker-init -- /nix/var/nix/p

root           7  0.0  0.0   5052  2240 ?        S    06:34   0:00 /run/dojo/bin/sleep 6h

root          68  0.0  0.0   4132  2560 ?        S    06:34   0:00 /challenge/32432-run-26634

root          72  0.0  0.0   2744  1280 ?        S    06:34   0:00 sleep 6h

hacker        73  0.0  0.0   5376  3840 pts/0    Ss   06:34   0:00 /run/dojo/bin/ssh-entrypoint

hacker       113  0.0  0.0   7868  3200 pts/0    R+   06:40   0:00 ps aux

hacker@processes~listing-processes:~$ /challenge/32432-run-26634

Yahaha, you found me! Here is your flag:

pwn.college{4a3W90exrJDhudSQk0Zc5EQSBTI.dhzM4QDL5ITO0czW}

Now I will sleep for a while (so that you could find me with 'ps').

### 2. Killing Processes

- [x] pwn.college{waRKMw5qZ8yXCE3lepeGhTGFh6q.dJDN4QDL5ITO0czW}

hacker@processes~killing-processes:~$ ps aux

USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND

root           1  0.0  0.0   1056   640 ?        Ss   06:53   0:00 /sbin/docker-init -- /nix/var/nix/p

root           7  0.0  0.0   5052  2560 ?        S    06:53   0:00 /run/dojo/bin/sleep 6h

root          71  0.0  0.0   4732  2880 ?        S    06:53   0:00 su -c /challenge/.launcher hacker

hacker        73  0.0  0.0   4976  3520 ?        Ss   06:53   0:00 /challenge/dont_run

hacker        74  0.0  0.0   5052  2560 ?        S    06:53   0:00 sleep 6h

hacker        75  0.0  0.0   5376  3840 pts/0    Ss   06:53   0:00 /run/dojo/bin/ssh-entrypoint

hacker        94  0.0  0.0   7868  3200 pts/0    R+   06:55   0:00 ps aux

hacker@processes~killing-processes:~$ kill 73

hacker@processes~killing-processes:~$ ps -e | grep dont

hacker@processes~killing-processes:~$ /challenge/run

Great job! Here is your payment:

pwn.college{waRKMw5qZ8yXCE3lepeGhTGFh6q.dJDN4QDL5ITO0czW}

### 3. Interrupting Processes

- [x] pwn.college{sXCx8xTO5cIfYmjg6mQ-WyZYp4P.dNDN4QDL5ITO0czW}

hacker@processes~interrupting-processes:~$ /challenge/run

I could give you the flag... but I won't, until this process exits. Remember,

you can force me to exit with Ctrl-C. Try it now!

^C

Good job! You have used Ctrl-C to interrupt this process! Here is your flag:

pwn.college{sXCx8xTO5cIfYmjg6mQ-WyZYp4P.dNDN4QDL5ITO0czW}

### 4. Suspending Processes

- [x] pwn.college{YPDCV-b_O3uiin0b-QduvQalHRk.dVDN4QDL5ITO0czW}

hacker@processes~suspending-processes:~$ /challenge/run

I'll only give you the flag if there's already another copy of me running in this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD

root          82      65  0 07:00 pts/0    00:00:00 bash /challenge/run

root          84      82  0 07:00 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can background me with Ctrl-Z or, if you're not ready to do that for whatever reason, just hit Enter and I'll exit!

^Z

[1]+  Stopped                 /challenge/run

hacker@processes~suspending-processes:~$ /challenge/run

I'll only give you the flag if there's already another copy of me running in this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD

root          82      65  0 07:00 pts/0    00:00:00 bash /challenge/run

root          89      65  0 07:00 pts/0    00:00:00 bash /challenge/run

root          91      89  0 07:00 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:

pwn.college{YPDCV-b_O3uiin0b-QduvQalHRk.dVDN4QDL5ITO0czW}

### 5. Resuming Processes

- [x] pwn.college{Y68lEY6Vwk9y_p20YpMYjMRWxeG.dZDN4QDL5ITO0czW}

hacker@processes~resuming-processes:~$ /challenge/run

Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with the 'fg' command! Or just press Enter to quit me!

^Z

[1]+  Stopped                 /challenge/run

hacker@processes~resuming-processes:~$ fg

/challenge/run

I'm back! Here's your flag:

pwn.college{Y68lEY6Vwk9y_p20YpMYjMRWxeG.dZDN4QDL5ITO0czW}

Don't forget to press Enter to quit me!

Goodbye!

#### Ctrl+c for stopping, Ctrl+z for pausing, fg for resuming

### 6. Backgrounding Processes

- [x] pwn.college{ggE-3hNXhQlLlvPoyOu6Ek69vji.ddDN4QDL5ITO0czW}

hacker@processes~backgrounding-processes:~$ /challenge/run

I'll only give you the flag if there's already another copy of me running *and not suspended* in this terminal... Let's check!

UID          PID STAT CMD

root          82 S+   bash /challenge/run

root          84 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the background, and then launch a new version of me! You can background me with Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to do that for whatever reason, just hit Enter and I'll exit!

^Z

[1]+  Stopped                 /challenge/run

hacker@processes~backgrounding-processes:~$ bg

[1]+ /challenge/run &



Yay, I'm now running the background! Because of that, this text will probably overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times to scroll this text out.

hacker@processes~backgrounding-processes:~$ /challenge/run

I'll only give you the flag if there's already another copy of me running *and not suspended* in this terminal... Let's check!

UID          PID STAT CMD

root          82 S    bash /challenge/run

root          92 S    sleep 6h

root          93 S+   bash /challenge/run

root          95 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:

pwn.college{ggE-3hNXhQlLlvPoyOu6Ek69vji.ddDN4QDL5ITO0czW} 

#### We were taught about the difference between fg and bg command

### 7. Foregrounding Processes

- [x] pwn.college{MnNH5xbaHFac-XlmjayM0TH3Sgy.dhDN4QDL5ITO0czW}

hacker@processes~foregrounding-processes:~$ /challenge/run

To pass this level, you need to suspend me, resume the suspended process in the background, and *then* foreground it without re-suspending it! You can background me with Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to do that for whatever reason, just hit Enter and I'll exit!

^Z

[1]+  Stopped                 /challenge/run

hacker@processes~foregrounding-processes:~$ bg

[1]+ /challenge/run &



Yay, I'm now running the background! Because of that, this text will probably overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times to scroll this text out. After that, resume me into the foreground with 'fg';

I'll wait.

hacker@processes~foregrounding-processes:~$ fg

/challenge/run

YES! Great job! I'm now running in the foreground. Hit Enter for your flag!

pwn.college{MnNH5xbaHFac-XlmjayM0TH3Sgy.dhDN4QDL5ITO0czW}

### 8. Starting Backgrounded Processes

- [x] pwn.college{kyuzLK1BZ3R53Zhlx5Md3Tm7ULf.dlDN4QDL5ITO0czW}

hacker@processes~starting-backgrounded-processes:~$ /challenge/run &

[1] 82

hacker@processes~starting-backgrounded-processes:~$


Yay, you started me in the background! Because of that, this text will probably overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!

pwn.college{kyuzLK1BZ3R53Zhlx5Md3Tm7ULf.dlDN4QDL5ITO0czW}

[1]+  Done                    /challenge/run

### 9. Process Exit Codes

- [x] pwn.college{Y4ah5yPOJGOhSwlNghX2JPZDlxD.dljN4UDL5ITO0czW}

hacker@processes~process-exit-codes:~$ /challenge/get-code

Exiting with an error code!

hacker@processes~process-exit-codes:~$ echo $?

187

hacker@processes~process-exit-codes:~$ /challenge/submit-code 187

CORRECT! Here is your flag:

pwn.college{Y4ah5yPOJGOhSwlNghX2JPZDlxD.dljN4UDL5ITO0czW}

