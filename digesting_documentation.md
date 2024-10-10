# Digesting Documentation

## Flags

### Learning from DOcumentation

- [x] pwn.college{EKV6ExGn6qlMTIgJRRLSjHqM6db.dRjM5QDL5ITO0czW}

hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{EKV6ExGn6qlMTIgJRRLSjHqM6db.dRjM5QDL5ITO0czW}


### Learning Complex Usage

- [x] pwn.college{0XecQMw3z0JbXNQ4LMPiQvvg0HY.dVjM5QDL5ITO0czW}

hacker@man~learning-complex-usage:~$ cd /
hacker@man~learning-complex-usage:/$ ls
bin   challenge  etc   home  lib32  libx32  mnt  opt   root  sbin  sys  usr
boot  dev        flag  lib   lib64  media   nix  proc  run   srv   tmp  var
hacker@man~learning-complex-usage:/$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{0XecQMw3z0JbXNQ4LMPiQvvg0HY.dVjM5QDL5ITO0czW}

### Reading Manuals

- [x] pwn.college{gsUENT-qn3aqtqFHfA5eIvgVJoO.dRTM4QDL5ITO0czW}

hacker@man~reading-manuals:~$ man challenge

CHALLENGE(1)             Challenge Commands             CHALLENGE(1)

NAME
       /challenge/challenge - print the flag!

SYNOPSIS
       challenge OPTION

DESCRIPTION
       Output the flag when called with the right arguments.

       --fortune
              read a fortune

       --version
              output version information and exit

       --gsqnaq NUM
              print the flag if NUM is 354

AUTHOR
       Written by Zardus.

REPORTING BUGS
       The  repository  for  this  dojo: <https://github.com/pwncol‐
       lege/linux-luminarium/>

SEE ALSO
       man(1) bash-builtins(7)

pwn.college                   May 2024                  CHALLENGE(1)
hacker@man~reading-manuals:~$ /challenge/challenge --gsnaq 354
Incorrect usage! Please read the challenge man page!
hacker@man~reading-manuals:~$ /challenge/challenge --gsqnaq 354
Correct usage! Your flag: pwn.college{gsUENT-qn3aqtqFHfA5eIvgVJoO.dRTM4QDL5ITO0czW}


### Searching Manuals

- [x]  pwn.college{ooEOoPOwC6RAjlD5dHRy6wuvGa_.dVTM4QDL5ITO0czW}

hacker@man~searching-manuals:~$ man challenge /
/run/workspace/bin/man: /: Is a directory
No manual entry for /
hacker@man~searching-manuals:~$ man challenge /flag
/run/workspace/bin/man: can't open /flag: Permission denied
hacker@man~searching-manuals:~$ man challenge / flag
/run/workspace/bin/man: /: Is a directory
No manual entry for /
No manual entry for flag
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --mwzxjyf
Initializing...
Correct usage! Your flag: pwn.college{ooEOoPOwC6RAjlD5dHRy6wuvGa_.dVTM4QDL5ITO0czW}

### Searching for Manuals

- [x] pwn.college{EF5GbzjIe_rETsroCFvW4uSj8F7.dZTM4QDL5ITO0czW}

hacker@man~searching-for-manuals:~$ man man
MAN(1)                        Manual pager utils                        MAN(1)

NAME
       man - an interface to the system reference manuals

SYNOPSIS
       man [man options] [[section] page ...] ...
       man -k [apropos options] regexp ...
       man -K [man options] [section] term ...
       man -f [whatis options] page ...
       man -l [man options] file ...
       man -w|-W [man options] page ...

DESCRIPTION
       man  is  the system's manual pager.  Each page argument given to man is
       normally the name of a program, utility or function.  The  manual  page
       associated with each of these arguments is then found and displayed.  A
       section, if provided, will direct man to look only in that  section  of
       the  manual.   The  default action is to search in all of the available
       sections following a pre-defined order (see DEFAULTS), and to show only
       the first page found, even if page exists in several sections.

       The table below shows the section numbers of the manual followed by the
       types of pages they contain.

       1   Executable programs or shell commands
       2   System calls (functions provided by the kernel)
       3   Library calls (functions within program libraries)
       4   Special files (usually found in /dev)
       5   File formats and conventions, e.g. /etc/passwd
       6   Games
hacker@man~searching-for-manuals:~$ man -k challenge
bzjersrovu (1)       - print the flag!
hacker@man~searching-for-manuals:~$ man bzjersrovu

CHALLENGE(1)                  Challenge Commands                  CHALLENGE(1)

NAME
       /challenge/challenge - print the flag!

SYNOPSIS
       challenge OPTION

DESCRIPTION
       Output the flag when called with the right arguments.

       --fortune
              read a fortune

       --version
              output version information and exit

       --bzjers NUM
              print the flag if NUM is 548

AUTHOR
       Written by Zardus.

REPORTING BUGS
       The  repository for this dojo: <https://github.com/pwncollege/linux-lu‐
       minarium/>

SEE ALSO
       man(1) bash-builtins(7)

hacker@man~searching-for-manuals:~$ /challenge/challenge --bzjers 548
Correct usage! Your flag: pwn.college{EF5GbzjIe_rETsroCFvW4uSj8F7.dZTM4QDL5ITO0czW}

### Helpful Programs

- [x] pwn.college{c_V3bgBFtqEwXq-s6eZr6ECiiyF.ddjM4QDL5ITO0czW}

hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v]
                                            [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give
                        you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 366
hacker@man~helpful-programs:~$ /challenge/challenge -g 366
Correct usage! Your flag: pwn.college{c_V3bgBFtqEwXq-s6eZr6ECiiyF.ddjM4QDL5ITO0czW}


### Help for Built-Ins

- [x] pwn.college{Qxdxt7QHZPlo0rLhm7F2tnJV9Fy.dRTM5QDL5ITO0czW}

hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "Qxdxt7QH".
hacker@man~help-for-builtins:~$ challenge --secret Qxdxt7QH
Correct! Here is your flag!
pwn.college{Qxdxt7QHZPlo0rLhm7F2tnJV9Fy.dRTM5QDL5ITO0czW}


 

