# File Globbing 

## Flags

### Matching with *

* is the wild character and can be used to replace any file which matches the pattern.
for the challenge /ch* changes the directory to /challenge
wherein you can run ./run to print the flag.


- [x] pwn.college{0xiuhPxGRFOK1ak_YhZt_kREhyM.dFjM4QDL5ITO0czW}

hacker@globbing~matching-with-:~$ cd /
hacker@globbing~matching-with-:/$ cd c*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{0xiuhPxGRFOK1ak_YhZt_kREhyM.dFjM4QDL5ITO0czW}
hacker@globbing~matching-with-:/challenge$


### Matching with ?

? is another wildcard character but it only replaces upto 1 character
following the same principle, we use cd /?ha??enge to change the directory, and then ./run to print the flag.


- [x] pwn.college{EnSqd-uVUHTGLyHc1PMOjEaSjfm.dJjM4QDL5ITO0czW}

This challenge resets your working directory to /home/hacker unless you change
directory properly...
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ ./run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{EnSqd-uVUHTGLyHc1PMOjEaSjfm.dJjM4QDL5ITO0czW}


### Matching with []

[] is like a wild-card multiple choice ie the pattern matching will only occur with the characters which are inside the [].
following instructions, cd /challenge/files
now as per challenge description we use [] to pass the arguments to /challenge/run ie /challenge/run file_[shab], this gives us the flag.

- [x] pwn.college{c1FBw4Ak5qZAWbQ-hrwBXUBdnHi.dNjM4QDL5ITO0czW} 

hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{c1FBw4Ak5qZAWbQ-hrwBXUBdnHi.dNjM4QDL5ITO0czW}


### Matching Paths with []

[] can be used to expand on absolute file paths as well.
/challenge/run /challenge/files/file_[absh] gives us the flag.

- [x] pwn.college{00pl5GvaK4b2l1bEtL2dFRqJv_2.dRjM4QDL5ITO0czW}

hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{00pl5GvaK4b2l1bEtL2dFRqJv_2.dRjM4QDL5ITO0czW}


### Mixing globs

This was a tricky one, following description we cd /challenge/files and see the files.
Interesting thing we notice is that there is only 1 filename with starting with each letter.
so [cep]* would expand to the file names we need
running /challenge/run [cep]* gives us the flag.

- [x] pwn.college{UFeXOyPYXqXvfK_1TrXJCiXlBM7.dVjM4QDL5ITO0czW}

hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ ls
amazing      fantastic   kind        pwning     uplifting   zesty
beautiful    great       laughing    queenly    victorious
challenging  happy       magical     radiant    wonderful
delightful   incredible  nice        splendid   xenial
educational  jovial      optimistic  thrilling  youthful
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{UFeXOyPYXqXvfK_1TrXJCiXlBM7.dVjM4QDL5ITO0czW} 

### Exclusionary Globbing 

[!<patter,letters>] the "!" or "^"acts as an invert and disincludes the chars in the "[]"
Similar to Challenge 5, we notice only 1 filename per letter in the /challenge/files directory
/challenge/run [!pwn]* gives us the flag.

- [x] pwn.college{A9FeXCz_lwnpHxmuSpgbxVOvio-.dZjM4QDL5ITO0czW}

hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{A9FeXCz_lwnpHxmuSpgbxVOvio-.dZjM4QDL5ITO0czW}
