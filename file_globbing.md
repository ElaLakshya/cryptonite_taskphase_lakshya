# File Globbing 

## Flags

### Matching with *

- [x] pwn.college{0xiuhPxGRFOK1ak_YhZt_kREhyM.dFjM4QDL5ITO0czW}

hacker@globbing~matching-with-:~$ cd /
hacker@globbing~matching-with-:/$ cd c*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{0xiuhPxGRFOK1ak_YhZt_kREhyM.dFjM4QDL5ITO0czW}
hacker@globbing~matching-with-:/challenge$


### Matching with ?

- [x] pwn.college{EnSqd-uVUHTGLyHc1PMOjEaSjfm.dJjM4QDL5ITO0czW}

This challenge resets your working directory to /home/hacker unless you change
directory properly...
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ ./run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{EnSqd-uVUHTGLyHc1PMOjEaSjfm.dJjM4QDL5ITO0czW}


### Matching with []

- [x] pwn.college{c1FBw4Ak5qZAWbQ-hrwBXUBdnHi.dNjM4QDL5ITO0czW} 

hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{c1FBw4Ak5qZAWbQ-hrwBXUBdnHi.dNjM4QDL5ITO0czW}


### Matching Paths with []

- [x] pwn.college{00pl5GvaK4b2l1bEtL2dFRqJv_2.dRjM4QDL5ITO0czW}

hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{00pl5GvaK4b2l1bEtL2dFRqJv_2.dRjM4QDL5ITO0czW}


### Mixing globs

- [x] 

### Exclusionary Globbing 

- [x] pwn.college{A9FeXCz_lwnpHxmuSpgbxVOvio-.dZjM4QDL5ITO0czW}

hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{A9FeXCz_lwnpHxmuSpgbxVOvio-.dZjM4QDL5ITO0czW}
