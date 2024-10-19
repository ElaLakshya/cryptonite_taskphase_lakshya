# Untangling Users

## Flag

``` 
### 1. Becoming Root with su

- [x] pwn.college{MTq5poGnLdRwhdMtlKhKdjRFSxE.dVTN0UDL5ITO0czW}

hacker@users~becoming-root-with-su:~$ su
Password:
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{MTq5poGnLdRwhdMtlKhKdjRFSxE.dVTN0UDL5ITO0czW}

### 2. Other users with su

- [x] pwn.college{goJ6XMHILCmEk8mUdvR7GWH0Wne.dZTN0UDL5ITO0czW}

hacker@users~other-users-with-su:~$ su zardus
Password:
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{goJ6XMHILCmEk8mUdvR7GWH0Wne.dZTN0UDL5ITO0czW} 

### 3. Cracking Passwords

- [x] pwn.college{sZdCdJ7WfSXj4wEqkIskXivgDkM.ddTN0UDL5ITO0czW}

hacker@users~cracking-passwords:~$ john /challenge/shadow-leak
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
aardvark         (zardus)
1g 0:00:00:22 100% 2/3 0.04508g/s 262.5p/s 262.5c/s 262.5C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ su zardus
Password:
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{sZdCdJ7WfSXj4wEqkIskXivgDkM.ddTN0UDL5ITO0czW}


### 4. Using sudo

- [x] pwn.college{cn1Wqwtiofhww58iyJO-3bcC_O9.dhTN0UDL5ITO0czW}

hacker@users~using-sudo:~$ sudo cat /flag
pwn.college{cn1Wqwtiofhww58iyJO-3bcC_O9.dhTN0UDL5ITO0czW}```
