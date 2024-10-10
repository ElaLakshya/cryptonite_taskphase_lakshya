# Pondetring_paths

## Flags

1) The Root : pwn.college{kEUfDwBuVVfz4sy0TBsH6R8ZD-O.dhzN5QDL5ITO0czW}

hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{kEUfDwBuVVfz4sy0TBsH6R8ZD-O.dhzN5QDL5ITO0czW}

2) Program and absolute paths : pwn.college{kUu0RbfZVZ5_ViJ7qxnDj0_PTom.dVDN1QDL5ITO0czW}

hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{kUu0RbfZVZ5_ViJ7qxnDj0_PTom.dVDN1QDL5ITO0czW}

3) Position thy self : pwn.college{8aRLKFWRRdEk09FAHVBchCledQP.dZDN1QDL5ITO0czW}

hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /usr/include directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd/usr/include
ssh-entrypoint: cd/usr/include: No such file or directory
hacker@paths~position-thy-self:~$ cd /usr/include
hacker@paths~position-thy-self:/usr/include$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{8aRLKFWRRdEk09FAHVBchCledQP.dZDN1QDL5ITO0czW}

4) Position Elsewhere : pwn.college{op5lZtc7o9Q7o_CDnzjgjkHQZY2.ddDN1QDL5ITO0czW}

hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /var/lib/apt/lists directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /var/lib/apt/lists
hacker@paths~position-elsewhere:/var/lib/apt/lists$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{op5lZtc7o9Q7o_CDnzjgjkHQZY2.ddDN1QDL5ITO0czW}

5) Position yet elsewhere : pwn.college{ITgcB88se9wxJne5As-LFAHMzEK.dhDN1QDL5ITO0czW} 

hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /sys directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /sys
hacker@paths~position-yet-elsewhere:/sys$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{ITgcB88se9wxJne5As-LFAHMzEK.dhDN1QDL5ITO0czW}

6) Implicit relative paths, from / : pwn.college{ozYhcwCW1Hd5WzTVvkSH7m6IY0d.dlDN1QDL5ITO0czW}

hacker@paths~implicit-relative-paths-from-:~$ /challenge/run
Incorrect...
You are not currently in the / directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ ./challenge/run
Incorrect...
This challenge must be invoked with a relative path that starts with a letter!
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{ozYhcwCW1Hd5WzTVvkSH7m6IY0d.dlDN1QDL5ITO0czW}

7) explicit Relative paths, from / : pwn.college{olxVWkWHzqo68cVWueD5WIKS809.dBTN1QDL5ITO0czW}

hacker@paths~explicit-relative-paths-from-:~$ /challenge/run
Incorrect...
You are not currently in the / directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{olxVWkWHzqo68cVWueD5WIKS809.dBTN1QDL5ITO0czW}

8) implicit relative path : pwn.college{UDy3J9nV4Nmx1VQRcsdmEcGw-EL.dFTN1QDL5ITO0czW}

hacker@paths~implicit-relative-path:~$ /challenge/run
Incorrect...
You are not currently in the /challenge directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ run
ssh-entrypoint: run: command not found
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{UDy3J9nV4Nmx1VQRcsdmEcGw-EL.dFTN1QDL5ITO0czW}

9) Home Sweet Home : pwn.college{kkrySc02aTEGS7mFuP_nuGVN8dM.dNzM4QDL5ITO0czW}

hacker@paths~home-sweet-home:~$ /chsllenge/run ~/a
ssh-entrypoint: /chsllenge/run: No such file or directory
hacker@paths~home-sweet-home:~$ /challenge/run ~/a
Writing the file to /home/hacker/a!
... and reading it back to you:
pwn.college{kkrySc02aTEGS7mFuP_nuGVN8dM.dNzM4QDL5ITO0czW}
