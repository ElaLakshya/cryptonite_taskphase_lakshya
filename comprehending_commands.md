# Comprehending Commands

## Flags

### Using ```cat```

cat flag gives us the flag.

- [x] pwn.college{0SeXsyORC14nv84w-eEsG0j0ghZ.dFzN1QDL5ITO0czW}

### catting absolute paths

running cd / gives us the directory where flag is located.
cat /opt/busybox/fs/flag gives us the flag.

- [x] pwn.college{w_GImKw0KPEZgqTlbq6ja_tOk1c.dlTM5QDL5ITO0czW}

### More catting practice



- [x] pwn.college{oYgG5F18PeYvve--NxuThWUvBMW.dBjM5QDL5ITO0czW}

### Gripping for a needle in a haystack

- [x] pwn.college{U8DtZ3Bywmaas_evx8t2F2anrGP.ddTM4QDL5ITO0czW}

### listing files

- [x] pwn.college{8-snCMGRVOcvEoJ8h_AvaWJMWs6.dhjM4QDL5ITO0czW}

### touching files

- [x] pwn.college{0k139KSHsaeCnxGa4kxSV-PaxYS.dBzM4QDL5ITO0czW}

### removing files

- [x] pwn.college{krYQP6a8I3zU9elzYaoJz495s94.dZTOwUDL5ITO0czW} 

### hidden files

- [x] pwn.college{MNiav7RdnCHw5M4Ct7Frqvpd3CH.dBTN4QDL5ITO0czW}

### An Epic Filesystem Quest

- [x] pwn.college{gyfSf-I2VWksT28iYKrCRDNBbah.dljM4QDL5ITO0czW}

### making directories

mkdir /tmp/pwn will make a directory
touch /tmp/pwn/college will make a file in the directory created as prescribed.
/challenge/run will print the flag.

- [x] pwn.college{MV4SrNzg74wTulI_9p_WnC-wj84.dFzM4QDL5ITO0czW}

### Finding Files

- [x] pwn.college{kZ9_GKBLs3gPjZpSD51w_6vC34L.dJzM4QDL5ITO0czW}

find / -name flag -type f will print the path to flag.
'/' tells the directory to search
-name is the name of the file
-type f specifies that we need to search files by default find searches for directories.


### linking files 

- [x] pwn.college{0-wWQeLcNtGBNhlRr7O74hLckXE.dlTM1UDL5ITO0czW}

    - we need create a symlink to the /flag directory
    - '/challenge/catflag' will read the the /home/hacker/not-the-flag file,
    - `ln -s /flag /home/hacker/not-the-flag` will create the soft link to not-the-flag file
    - `/challenge/catflag` copy and read out the flag from 'not-the-flag' thus printing the flag to the terminal. 


