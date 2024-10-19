# Chaining Commands

## Flags

```
### 1. Chaining with semicolons

- [x] pwn.college{IDugrKrGh2BxHMuCbVHytFhyViM.dVTN4QDL5ITO0czW}

hacker@chaining~chaining-with-semicolons:~$ /challenge/pwn; /challenge/college
Yes! You chained /challenge/pwn and /challenge/college! Here is your flag:
pwn.college{IDugrKrGh2BxHMuCbVHytFhyViM.dVTN4QDL5ITO0czW}

### 2. Your first shell script

- [x] pwn.college{MFnBVQXvDkdxceKDEnVor5IhKJ7.dFzN4QDL5ITO0czW}

hacker@chaining~your-first-shell-script:~$ touch x.sh
hacker@chaining~your-first-shell-script:~$ nano x.sh
hacker@chaining~your-first-shell-script:~$ bash x.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{MFnBVQXvDkdxceKDEnVor5IhKJ7.dFzN4QDL5ITO0czW}

### 3. Redirecting Script Output

- [x] pwn.college{gKifnHcNWntyERWQ_ovWHyvLkGD.dhTM5QDL5ITO0czW}

hacker@chaining~redirecting-script-output:~$ touch x.sh
hacker@chaining~redirecting-script-output:~$ nano x.sh
hacker@chaining~redirecting-script-output:~$ bash x.sh | /challenge/solve
Correct! Here is your flag:
pwn.college{gKifnHcNWntyERWQ_ovWHyvLkGD.dhTM5QDL5ITO0czW}

### 4. Executable Shell Scripts

- [x] pwn.college{kHwGyWgHayWzqTYWJMB2mlIYcrm.dRzNyUDL5ITO0czW}

hacker@chaining~executable-shell-scripts:~$ touch x.sh
hacker@chaining~executable-shell-scripts:~$ nano x.sh
hacker@chaining~executable-shell-scripts:~$ ls -l x.sh
-rw-r--r-- 1 hacker hacker 17 Oct 19 17:43 x.sh
hacker@chaining~executable-shell-scripts:~$ chmod ugo=rwx x.sh
hacker@chaining~executable-shell-scripts:~$ ls -l x.sh
-rwxrwxrwx 1 hacker hacker 17 Oct 19 17:43 x.sh
hacker@chaining~executable-shell-scripts:~$ ./x.sh
Congratulations on your shell script execution! Your flag:
pwn.college{kHwGyWgHayWzqTYWJMB2mlIYcrm.dRzNyUDL5ITO0czW} 
```
