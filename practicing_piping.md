# Practicing Piping

## Flags

### Redirecting Output

- [x] pwn.college{4xJ7rXaF6GRe4Z2naa02wEYqgCs.dRjN1QDL5ITO0czW}

hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your
flag:
pwn.college{4xJ7rXaF6GRe4Z2naa02wEYqgCs.dRjN1QDL5ITO0czW}

### REDIRECTING MORE OUTPUT

- [x] pwn.college{soM5_8ftzZQIjNvPeCsGA5htDna.dVjN1QDL5ITO0czW}

hacker@piping~redirecting-more-output:~$ /challenge/run
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag
[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[FAIL] You did not satisfy all the execution requirements.
[FAIL] Specifically, you must fix the following issue:
[FAIL]   You have not redirected anything for this process' stdout.
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag
[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{soM5_8ftzZQIjNvPeCsGA5htDna.dVjN1QDL5ITO0czW}

### Appending Output

- [x] pwn.college{0btH7126dpIO3rKRWLO2XFvRQZl.ddDM5QDL5ITO0czW} 

hacker@piping~appending-output:~$ /challenge/run >> /home/hacker/the-flag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] Good luck!

[TEST] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
I will write the flag in two parts to the file /home/hacker/the-flag! I'll do
the first write directly to the file, and the second write, I'll do to stdout
(if it's pointing at the file). If you redirect the output in append mode, the
second write will append to (rather than overwrite) the first write, and you'll
get the whole flag!
hacker@piping~appending-output:~$ cat the-flag
 |
\|/ This is the first half:
 v
pwn.college{0btH7126dpIO3rKRWLO2XFvRQZl.ddDM5QDL5ITO0czW}
                              ^
     that is the second half /|\
                              |

If you only see the second half above, you redirected in *truncate* mode (>)
rather than *append* mode (>>), and so the write of the second half to stdout
overwrote the initial write of the first half directly to the file. Try append

mode!

### Redirecting Errors

- [x] pwn.college{Q8ary6I97XJtxq_Pv2daDsADTYp.ddjN1QDL5ITO0czW}

hacker@piping~redirecting-errors:~$ /challenge/run
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will check that error output is redirected to a specific file path : instructions
[INFO] - the challenge will output a reward file if all the tests pass : /flag
[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[FAIL] You did not satisfy all the execution requirements.
[FAIL] Specifically, you must fix the following issue:
[FAIL]   You have not redirected anything for this process' stdout.
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat fl
cat: fl: No such file or directory
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{Q8ary6I97XJtxq_Pv2daDsADTYp.ddjN1QDL5ITO0czW}

### Redirecting Input 

- [x] pwn.college{ofLgsjXwokuOq37ucRasfRRc8Qe.dBzN1QDL5ITO0czW}

hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{ofLgsjXwokuOq37ucRasfRRc8Qe.dBzN1QDL5ITO0czW}

### Grepping Stored Results

- [x] pwn.college{swWeNeWJ17PEdFvRQ5tzZ1nP1Ld.dhTM4QDL5ITO0czW}

hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to a file called /tmp/data.txt. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~grepping-stored-results:~$ grep /tmp/data.txt pwn.college
grep: pwn.college: No such file or directory
hacker@piping~grepping-stored-results:~$ grep pwn.college /tmp/data.txt
pwn.college{swWeNeWJ17PEdFvRQ5tzZ1nP1Ld.dhTM4QDL5ITO0czW}

### Grepping Live Output

- [x] pwn.college{8mvBbt91KriQrV4pvAtfnF4Jkm5.dlTM4QDL5ITO0czW}

hacker@piping~grepping-live-output:~$ /challenge/run | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stdout : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/xpq4yhadyhazkcsggmqd7rsgvxb3kjy4-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{8mvBbt91KriQrV4pvAtfnF4Jkm5.dlTM4QDL5ITO0czW}

### Grepping Errors

- [x] pwn.college{QQxS87DZFALlyooSLfSo1y8eomE.dVDM5QDL5ITO0czW}

hacker@piping~grepping-errors:~$ /challenge/run 2>&1 | grep pwn.colle
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/xpq4yhadyhazkcsggmqd7rsgvxb3kjy4-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{QQxS87DZFALlyooSLfSo1y8eomE.dVDM5QDL5ITO0czW}

### Duplicating Data with tee


- [x] pwn.college{wbC2VkWFeYWfTFSHoBvHLZ_kOpv.dFjM5QDL5ITO0czW}

hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee out.txt | /challenge/college
Processing...
WARNING: you are overwriting file out.txt with tee's output...
The input to 'college' does not contain the correct secret code! This code
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat out.txt
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "wbC2VkWF"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret wbC2VkWF | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{wbC2VkWFeYWfTFSHoBvHLZ_kOpv.dFjM5QDL5ITO0czW}


### Writing to multiple programs

- [x] pwn.college{QdC8Pgzr_re2J8pi9L1ERNqNS29.dBDO0UDL5ITO0czW}

hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) >(/challenge/planet)

This secret data must directly and simultaneously make it to /challenge/the and
/challenge/planet. Don't try to copy-paste it; it changes too fast.
4461497063053417

Congratulations, you have duplicated data into the input of two programs! Here
is your flag:

pwn.college{QdC8Pgzr_re2J8pi9L1ERNqNS29.dBDO0UDL5ITO0czW}

### Split-piping stderr and stdout

- [x] pwn.college{cg1wuCgnrLjhcjedlrSYpuuNPrw.dFDNwYDL5ITO0czW}

hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack > >(/challenge/planet) 2> >(/challenge/the)

Congratulations, you have learned a redirection technique that even experts
struggle with! Here is your flag:

pwn.college{cg1wuCgnrLjhcjedlrSYpuuNPrw.dFDNwYDL5ITO0czW}
