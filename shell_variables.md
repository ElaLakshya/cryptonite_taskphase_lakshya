# Shell Variables

## Flags

### Printing Variables

- [x] pwn.college{4Wq9-3eKIab-RmrNZLEb2kgDKP7.ddTN1QDL5ITO0czW}

hacker@variables~printing-variables:~$ echo $FLAG

pwn.college{4Wq9-3eKIab-RmrNZLEb2kgDKP7.ddTN1QDL5ITO0czW}

This module was rather simple given we were told to output using a simple command as echo and $<variable>


### Setting Variables

- [x] pwn.college{QI2Q0YcMzTGmnYZQusGT_4r4CAD.dlTN1QDL5ITO0czW}

hacker@variables~setting-variables:~$ PWN=COLLEGE

You've set the PWN variable properly! As promised, here is the flag:

pwn.college{QI2Q0YcMzTGmnYZQusGT_4r4CAD.dlTN1QDL5ITO0czW}

### Multi-Word Variables

- [x] pwn.college{M13zYTxthWRdjyQds1Vv6yqRph7.dBjN1QDL5ITO0czW}

hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"

You've set the PWN variable properly! As promised, here is the flag:

pwn.college{M13zYTxthWRdjyQds1Vv6yqRph7.dBjN1QDL5ITO0czW}


### Exporting Variables

- [x] pwn.college{wg_zlG1ib1cvjXy5hp2Hrx8sMZX.dJjN1QDL5ITO0czW}

hacker@variables~exporting-variables:~$ export PWN=COLLEGE

You've set the PWN variable to the proper value!

hacker@variables~exporting-variables:~$ COLLEGE=PWN

You've set the PWN variable to the proper value!

You've set the COLLEGE variable to the proper value!

hacker@variables~exporting-variables:~$ /challenge/run

CORRECT!

You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great

job! Here is your flag:

pwn.college{wg_zlG1ib1cvjXy5hp2Hrx8sMZX.dJjN1QDL5ITO0czW}

You've set the PWN variable to the proper value!

You've set the COLLEGE variable to the proper value!
 
#### Exporting variables was simple but we didn't practice the sh and $ command

### Printing Exported Variables

- [x] pwn.college{87cW1rmDIRvf4jkPwBmByKhoQ6c.dhTN1QDL5ITO0czW}

hacker@variables~printing-exported-variables:~$ env

SHELL=/run/dojo/bin/bash

HOSTNAME=variables~printing-exported-variables

PWD=/home/hacker

DOJO_AUTH_TOKEN=d2ee077b337b7a78d873d6500abd4c4aa1ccb785b4d6dccf40c3d4eb0d4aeca0
HOME=/home/hacker

LANG=C.UTF-8

LS_COLORS=rs=0:di=01;....

FLAG=pwn.college{87cW1rmDIRvf4jkPwBmByKhoQ6c.dhTN1QDL5ITO0czW}

LESSCLOSE=/usr/bin/lesspipe %s %s

TERM=xterm

LESSOPEN=| /usr/bin/lesspipe %s

SHLVL=1

LC_CTYPE=C.UTF-8

PATH=/run/challenge/bin:/run/workspace/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin

_=/run/workspace/bin/env

hacker@variables~printing-exported-variables:~$ env | grep FLAG

FLAG=pwn.college{87cW1rmDIRvf4jkPwBmByKhoQ6c.dhTN1QDL5ITO0czW}

#### In this exercise we could've simply found the FLAG variable in the huge amount of data but I tried to use piping and succeeded

### Storing Command Output

- [x] pwn.college{EswX_sJVLYpcZTsEk5d_JL02ROh.dVzN0UDL5ITO0czW}

hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)

Congratulations! You have read the flag into the PWN variable. Now print it out and submit it!

hacker@variables~storing-command-output:~$ echo $PWN

pwn.college{EswX_sJVLYpcZTsEk5d_JL02ROh.dVzN0UDL5ITO0czW}

#### Usinf Variables to store command output feels extremely convinient. I think it will help reduce a lot of hardwork in more complex problems.

### Reading Input

- [x] pwn.college{ADrHzW18hqcJnPRMmIYfUELK83V.dhzN1QDL5ITO0czW}

hacker@variables~reading-input:~$ read -p "PWN = " PWN

PWN = COLLEGE

You've set the PWN variable properly! As promised, here is the flag:

pwn.college{ADrHzW18hqcJnPRMmIYfUELK83V.dhzN1QDL5ITO0czW}

#### Reading Variables from the USER is an important part of problem solving.

### Reading files

- [x] pwn.college{4S7ZAz__23j7oxUKXNz_xyhiRqF.dBjM4QDL5ITO0czW}

hacker@variables~reading-files:~$ read PWN < /challenge/read_me

You've set the PWN variable properly! As promised, here is the flag:

pwn.college{4S7ZAz__23j7oxUKXNz_xyhiRqF.dBjM4QDL5ITO0czW}

