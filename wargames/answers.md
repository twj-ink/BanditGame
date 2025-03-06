level 0:
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```
-> level 1:

```bash
bandit0@bandit:~$ ls
readme
bandit0@bandit:~$ cat readme
Congratulations on your first steps into the bandit game!!
Please make sure you have read the rules at https://overthewire.org/rules/
If you are following a course, workshop, walkthrough or other educational activity,
please inform the instructor about the rules as well and encourage them to
contribute to the OverTheWire community so we can keep these games free!

The password you are looking for is: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
```

-> level 2:

```bash
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat ./-
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
```

-> level 3:

```bash
bandit2@bandit:~$ ls
spaces in this filename

bandit2@bandit:~$ cat spaces\ in\ this\ filename
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

bandit2@bandit:~$ cat "spaces in this filename"
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

bandit2@bandit:~$ cat 'spaces in this filename'
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

bandit2@bandit:~$ cat spaces in this filename
cat: spaces: No such file or directory
cat: in: No such file or directory
cat: this: No such file or directory
cat: filename: No such file or directory
```

-> level 4:

```bash
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ ls -l
total 4
drwxr-xr-x 2 root root 4096 Sep 19 07:08 inhere
bandit3@bandit:~$ ls -a
.  ..  .bash_logout  .bashrc  inhere  .profile
bandit3@bandit:~$ cat inhere
cat: inhere: Is a directory
bandit3@bandit:~$ cd inhere/
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ ls -a
.  ..  ...Hiding-From-You
bandit3@bandit:~/inhere$ cat ...Hiding-From-You
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
```

-> level 5:

```bash
bandit4@bandit:~/inhere$ ls
-file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09
bandit4@bandit:~/inhere$ file -file00
file: Cannot open `ile00' (No such file or directory)
bandit4@bandit:~/inhere$ file ./-file00
./-file00: data
bandit4@bandit:~/inhere$ file ./-file01
./-file01: data
bandit4@bandit:~/inhere$ file ./-file02
./-file02: data
bandit4@bandit:~/inhere$ file ./-file03
./-file03: data
bandit4@bandit:~/inhere$ file ./-file04
./-file04: data
bandit4@bandit:~/inhere$ file ./-file05
./-file05: data
bandit4@bandit:~/inhere$ file ./-file06
./-file06: data
bandit4@bandit:~/inhere$ file ./-file07
./-file07: ASCII text
bandit4@bandit:~/inhere$ file ./-file08
./-file08: data
bandit4@bandit:~/inhere$ file ./-file09
./-file09: data

bandit4@bandit:~/inhere$ cat ./-file07
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
```

-> level 6:

```bash
bandit5@bandit:~/inhere$ ls
maybehere00  maybehere03  maybehere06  maybehere09  maybehere12  maybehere15  maybehere18
maybehere01  maybehere04  maybehere07  maybehere10  maybehere13  maybehere16  maybehere19
maybehere02  maybehere05  maybehere08  maybehere11  maybehere14  maybehere17

bandit5@bandit:~/inhere$ find . -type f -size 1033c
./maybehere07/.file2

bandit5@bandit:~/inhere$ file ./maybehere07/.file2
./maybehere07/.file2: ASCII text, with very long lines (1000)

bandit5@bandit:~/inhere$ ls -l ./maybehere07/.file2
-rw-r----- 1 root bandit5 1033 Sep 19 07:08 ./maybehere07/.file2

bandit5@bandit:~/inhere$ cd maybehere07
bandit5@bandit:~/inhere/maybehere07$ cat ./.file2
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        
                                        bandit5@bandit:~/inhere/maybehere07$
```

-> level 7:

```bash
bandit6@bandit:~$ find / -group bandit6 -user bandit7 -size 33c
find: ‘/drifter/drifter14_src/axTLS’: Permission denied
find: ‘/root’: Permission denied
find: ‘/snap’: Permission denied
find: ‘/tmp’: Permission denied
find: ‘/proc/tty/driver’: Permission denied
find: ‘/proc/1837157/task/1837157/fd/6’: No such file or directory
find: ‘/proc/1837157/task/1837157/fdinfo/6’: No such file or directory
find: ‘/proc/1837157/fd/5’: No such file or directory
find: ‘/proc/1837157/fdinfo/5’: No such file or directory
find: ‘/home/bandit31-git’: Permission denied
find: ‘/home/ubuntu’: Permission denied
find: ‘/home/bandit5/inhere’: Permission denied
find: ‘/home/bandit30-git’: Permission denied
find: ‘/home/drifter8/chroot’: Permission denied
find: ‘/home/drifter6/data’: Permission denied
find: ‘/home/bandit29-git’: Permission denied
find: ‘/home/bandit28-git’: Permission denied
find: ‘/home/bandit27-git’: Permission denied
find: ‘/lost+found’: Permission denied
find: ‘/etc/polkit-1/rules.d’: Permission denied
find: ‘/etc/multipath’: Permission denied
find: ‘/etc/stunnel’: Permission denied
find: ‘/etc/xinetd.d’: Permission denied
find: ‘/etc/credstore.encrypted’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
find: ‘/etc/sudoers.d’: Permission denied
find: ‘/etc/credstore’: Permission denied
find: ‘/dev/shm’: Permission denied
find: ‘/dev/mqueue’: Permission denied
find: ‘/var/log/amazon’: Permission denied
find: ‘/var/log/unattended-upgrades’: Permission denied
find: ‘/var/log/chrony’: Permission denied
find: ‘/var/log/private’: Permission denied
find: ‘/var/tmp’: Permission denied
find: ‘/var/spool/cron/crontabs’: Permission denied
find: ‘/var/spool/bandit24’: Permission denied
find: ‘/var/spool/rsyslog’: Permission denied
find: ‘/var/cache/ldconfig’: Permission denied
find: ‘/var/cache/apt/archives/partial’: Permission denied
find: ‘/var/cache/pollinate’: Permission denied
find: ‘/var/cache/private’: Permission denied
find: ‘/var/cache/apparmor/2425d902.0’: Permission denied
find: ‘/var/cache/apparmor/baad73a1.0’: Permission denied
find: ‘/var/lib/polkit-1’: Permission denied
find: ‘/var/lib/amazon’: Permission denied
/var/lib/dpkg/info/bandit7.password
find: ‘/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/chrony’: Permission denied
find: ‘/var/lib/snapd/void’: Permission denied
find: ‘/var/lib/snapd/cookie’: Permission denied
find: ‘/var/lib/private’: Permission denied
find: ‘/var/lib/ubuntu-advantage/apt-esm/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/update-notifier/package-data-downloads/partial’: Permission denied
find: ‘/var/lib/udisks2’: Permission denied
find: ‘/var/crash’: Permission denied
find: ‘/boot/efi’: Permission denied
find: ‘/boot/lost+found’: Permission denied
find: ‘/sys/kernel/tracing’: Permission denied
find: ‘/sys/kernel/debug’: Permission denied
find: ‘/sys/fs/pstore’: Permission denied
find: ‘/sys/fs/bpf’: Permission denied
find: ‘/run/lock/lvm’: Permission denied
find: ‘/run/systemd/inaccessible/dir’: Permission denied
find: ‘/run/systemd/propagate/systemd-udevd.service’: Permission denied
find: ‘/run/systemd/propagate/systemd-resolved.service’: Permission denied
find: ‘/run/systemd/propagate/systemd-networkd.service’: Permission denied
find: ‘/run/systemd/propagate/irqbalance.service’: Permission denied
find: ‘/run/systemd/propagate/systemd-logind.service’: Permission denied
find: ‘/run/systemd/propagate/chrony.service’: Permission denied
find: ‘/run/systemd/propagate/polkit.service’: Permission denied
find: ‘/run/systemd/propagate/ModemManager.service’: Permission denied
find: ‘/run/systemd/propagate/fwupd.service’: Permission denied
find: ‘/run/lvm’: Permission denied
find: ‘/run/cryptsetup’: Permission denied
find: ‘/run/multipath’: Permission denied
find: ‘/run/screen/S-bandit20’: Permission denied
find: ‘/run/screen/S-bandit21’: Permission denied
find: ‘/run/screen/S-bandit22’: Permission denied
find: ‘/run/sudo’: Permission denied
find: ‘/run/user/11012’: Permission denied
find: ‘/run/user/11027’: Permission denied
find: ‘/run/user/11016’: Permission denied
find: ‘/run/user/11006/systemd/inaccessible/dir’: Permission denied
find: ‘/run/user/11000’: Permission denied
find: ‘/run/user/11005’: Permission denied
find: ‘/run/user/11009’: Permission denied
find: ‘/run/user/11001’: Permission denied
find: ‘/run/user/11004’: Permission denied
find: ‘/run/user/11020’: Permission denied
find: ‘/run/user/11013’: Permission denied
find: ‘/run/user/11011’: Permission denied
find: ‘/run/user/11014’: Permission denied
find: ‘/run/user/11008’: Permission denied
find: ‘/run/user/11032’: Permission denied
find: ‘/run/user/11031’: Permission denied
find: ‘/run/user/11024’: Permission denied
find: ‘/run/user/11010’: Permission denied
find: ‘/run/user/11023’: Permission denied
find: ‘/run/user/11002’: Permission denied
find: ‘/run/user/11025’: Permission denied
find: ‘/run/user/11007’: Permission denied
find: ‘/run/user/11022’: Permission denied
find: ‘/run/user/11003’: Permission denied
find: ‘/run/user/11015’: Permission denied
find: ‘/run/user/11026’: Permission denied
find: ‘/run/chrony’: Permission denied
find: ‘/run/udisks2’: Permission denied

bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
```

-> level 8：

```bash
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ ls -l
total 4088
-rw-r----- 1 bandit8 bandit7 4184396 Sep 19 07:08 data.txt
bandit7@bandit:~$ grep 'millionth' data.txt
millionth       dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
```

-> level 9:

```bash
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ ls -la
total 56
drwxr-xr-x  2 root    root     4096 Sep 19 07:08 .
drwxr-xr-x 70 root    root     4096 Sep 19 07:09 ..
-rw-r--r--  1 root    root      220 Mar 31  2024 .bash_logout
-rw-r--r--  1 root    root     3771 Mar 31  2024 .bashrc
-rw-r-----  1 bandit9 bandit8 33033 Sep 19 07:08 data.txt
-rw-r--r--  1 root    root      807 Mar 31  2024 .profile
bandit8@bandit:~$ sort data.txt | uniq -u
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
```

-> level 10:

```bash
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ strings data.txt | grep =
}========== the
p\l=
;c<Q=.dEXU!
3JprD========== passwordi
qC(=
~fDV3========== is
7=oc
zP=
~de=
3k=fQ
~o=0
69}=
%"=Y
=tZ~07
D9========== FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
N=~[!N
zA=?0j
```

-> level 11:

```bash
bandit10@bandit:~$ ls -l
total 4
-rw-r----- 1 bandit11 bandit10 69 Sep 19 07:08 data.txt
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIGR0UjE3M2ZaS2IwUlJzREZTR3NnMlJXbnBOVmozcVJyCg==
bandit10@bandit:~$ base64 -d data.txt
The password is dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
```

-> level 12:

```bash
bandit11@bandit:~$ ls -l
total 4
-rw-r----- 1 bandit12 bandit11 49 Sep 19 07:08 data.txt
bandit11@bandit:~$ tr 'a-zA-Z' 'n-za-mN-ZA-M' < data.txt
The password is 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
```

-> level 13:

```bash
bandit12@bandit:~$ cd /tmp
bandit12@bandit:/tmp$ ls
ls: cannot open directory '.': Permission denied
bandit12@bandit:/tmp$ mkdir myans
bandit12@bandit:/tmp$ ls
ls: cannot open directory '.': Permission denied
bandit12@bandit:/tmp$ cd myans
bandit12@bandit:/tmp/myans$ ls
bandit12@bandit:/tmp/myans$ ls -l
total 0
bandit12@bandit:/tmp/myans$ cp ~/data.txt .
bandit12@bandit:/tmp/myans$ ls
data.txt
bandit12@bandit:/tmp/myans$ man mv
bandit12@bandit:/tmp/myans$ mv data.txt hex_data.txt
bandit12@bandit:/tmp/myans$ ls
hex_data.txt

bandit12@bandit:/tmp/myans$ file hex_data.txt
hex_data.txt: ASCII text
bandit12@bandit:/tmp/myans$
bandit12@bandit:/tmp/myans$ ls
hex_data.txt
bandit12@bandit:/tmp/myans$ cat hex_data.txt
00000000: 1f8b 0808 dfcd eb66 0203 6461 7461 322e  .......f..data2.
00000010: 6269 6e00 013e 02c1 fd42 5a68 3931 4159  bin..>...BZh91AY
00000020: 2653 59ca 83b2 c100 0017 7fff dff3 f4a7  &SY.............
00000030: fc9f fefe f2f3 cffe f5ff ffdd bf7e 5bfe  .............~[.
00000040: faff dfbe 97aa 6fff f0de edf7 b001 3b56  ......o.......;V
00000050: 0400 0034 d000 0000 0069 a1a1 a000 0343  ...4.....i.....C
00000060: 4686 4341 a680 068d 1a69 a0d0 0068 d1a0  F.CA.....i...h..
00000070: 1906 1193 0433 5193 d4c6 5103 4646 9a34  .....3Q...Q.FF.4
00000080: 0000 d320 0680 0003 264d 0346 8683 d21a  ... ....&M.F....
00000090: 0686 8064 3400 0189 a683 4fd5 0190 001e  ...d4.....O.....
000000a0: 9034 d188 0343 0e9a 0c40 69a0 0626 4686  .4...C...@i..&F.
000000b0: 8340 0310 d340 3469 a680 6800 0006 8d0d  .@...@4i..h.....
000000c0: 0068 0608 0d1a 64d3 469a 1a68 c9a6 8030  .h....d.F..h...0
000000d0: 9a68 6801 8101 3204 012a ca60 51e8 1cac  .hh...2..*.`Q...
000000e0: 532f 0b84 d4d0 5db8 4e88 e127 2921 4c8e  S/....].N..')!L.
000000f0: b8e6 084c e5db 0835 ff85 4ffc 115a 0d0c  ...L...5..O..Z..
00000100: c33d 6714 0121 5762 5e0c dbf1 aef9 b6a7  .=g..!Wb^.......
00000110: 23a6 1d7b 0e06 4214 01dd d539 af76 f0b4  #..{..B....9.v..
00000120: a22f 744a b61f a393 3c06 4e98 376f dc23  ./tJ....<.N.7o.#
00000130: 45b1 5f23 0d8f 640b 3534 de29 4195 a7c6  E._#..d.54.)A...
00000140: de0c 744f d408 4a51 dad3 e208 189b 0823  ..tO..JQ.......#
00000150: 9fcc 9c81 e58c 9461 9dae ce4a 4284 1706  .......a...JB...
00000160: 61a3 7f7d 1336 8322 cd59 e2b5 9f51 8d99  a..}.6.".Y...Q..
00000170: c300 2a9d dd30 68f4 f9f6 7db6 93ea ed9a  ..*..0h...}.....
00000180: dd7c 891a 1221 0926 97ea 6e05 9522 91f1  .|...!.&..n.."..
00000190: 7bd3 0ba4 4719 6f37 0c36 0f61 02ae dea9  {...G.o7.6.a....
000001a0: b52f fc46 9792 3898 b953 36c4 c247 ceb1  ./.F..8..S6..G..
000001b0: 8a53 379f 4831 52a3 41e9 fa26 9d6c 28f4  .S7.H1R.A..&.l(.
000001c0: 24ea e394 651d cb5c a96c d505 d986 da22  $...e..\.l....."
000001d0: 47f4 d58b 589d 567a 920b 858e a95c 63c1  G...X.Vz.....\c.
000001e0: 2509 612c 5364 8e7d 2402 808e 9b60 02b4  %.a,Sd.}$....`..
000001f0: 13c7 be0a 1ae3 1400 4796 4370 efc0 9b43  ........G.Cp...C
00000200: a4cb 882a 4aae 4b81 abf7 1c14 67f7 8a34  ...*J.K.....g..4
00000210: 0867 e5b6 1df6 b0e8 8023 6d1c 416a 28d0  .g.......#m.Aj(.
00000220: c460 1604 bba3 2e52 297d 8788 4e30 e1f9  .`.....R)}..N0..
00000230: 2646 8f5d 3062 2628 c94e 904b 6754 3891  &F.]0b&(.N.KgT8.
00000240: 421f 4a9f 9feb 2ec9 83e2 c20f fc5d c914  B.J..........]..
00000250: e142 432a 0ecb 0459 1b15 923e 0200 00    .BC*...Y...>...
bandit12@bandit:/tmp/myans$ file hex_data.txt
hex_data.txt: ASCII text
bandit12@bandit:/tmp/myans$ xxd -r hex_data.txt > data.bin
bandit12@bandit:/tmp/myans$ file data.bin
data.bin: gzip compressed data, was "data2.bin", last modified: Thu Sep 19 07:08:15 2024, max compression, from Unix, original size modulo 2^32 574
bandit12@bandit:/tmp/myans$ gunzip data.bin > data1.bin
gzip: data.bin: unknown suffix -- ignored
bandit12@bandit:/tmp/myans$ ls
data1.bin  data.bin  hex_data.txt
bandit12@bandit:/tmp/myans$ file ./*
./data1.bin:    empty
./data.bin:     gzip compressed data, was "data2.bin", last modified: Thu Sep 19 07:08:15 2024, max compression, from Unix, original size modulo 2^32 574
./hex_data.txt: ASCII text
bandit12@bandit:/tmp/myans$ mv data.bin data.bin.gz
bandit12@bandit:/tmp/myans$ gunzip data.bin.gz > data1.bin
bandit12@bandit:/tmp/myans$ ls
data1.bin  data.bin  hex_data.txt
bandit12@bandit:/tmp/myans$ file ./*
./data1.bin:    empty
./data.bin:     bzip2 compressed data, block size = 900k
./hex_data.txt: ASCII text
bandit12@bandit:/tmp/myans$ rm data1.bin data.bin
bandit12@bandit:/tmp/myans$ xxd -r hex_data.txt > d.bin
bandit12@bandit:/tmp/myans$ mv d.bin  d.bin.gz
bandit12@bandit:/tmp/myans$ gunzip -c d.bin.gz > d1.bin
bandit12@bandit:/tmp/myans$ ls
d1.bin  d.bin.gz  hex_data.txt
bandit12@bandit:/tmp/myans$ file *
d1.bin:       bzip2 compressed data, block size = 900k
d.bin.gz:     gzip compressed data, was "data2.bin", last modified: Thu Sep 19 07:08:15 2024, max compression, from Unix, original size modulo 2^32 574
hex_data.txt: ASCII text
bandit12@bandit:/tmp/myans$ bunzip2 -c d1.bin > d2.bin
bandit12@bandit:/tmp/myans$ ls
d1.bin  d2.bin  d.bin.gz  hex_data.txt
bandit12@bandit:/tmp/myans$ file *
d1.bin:       bzip2 compressed data, block size = 900k
d2.bin:       gzip compressed data, was "data4.bin", last modified: Thu Sep 19 07:08:15 2024, max compression, from Unix, original size modulo 2^32 20480
d.bin.gz:     gzip compressed data, was "data2.bin", last modified: Thu Sep 19 07:08:15 2024, max compression, from Unix, original size modulo 2^32 574
bandit12@bandit:/tmp/myans$
bandit12@bandit:/tmp/myans$ mv d2.bin d2.bin.gz
bandit12@bandit:/tmp/myans$ gunzip -c d2.bin.gz > d3.bin
bandit12@bandit:/tmp/myans$ ls
d1.bin  d2.bin.gz  d3.bin  d.bin.gz  hex_data.txt
bandit12@bandit:/tmp/myans$ file d3.bin
d3.bin: POSIX tar archive (GNU)
bandit12@bandit:/tmp/myans$ mkdir extracted_files
bandit12@bandit:/tmp/myans$ ls
d1.bin  d2.bin.gz  d3.bin  d.bin.gz  extracted_files  hex_data.txt
bandit12@bandit:/tmp/myans$ tar -xvf d3.bin -C extracted_files/
data5.bin
bandit12@bandit:/tmp/myans$ ls
d1.bin  d2.bin.gz  d3.bin  d.bin.gz  extracted_files  hex_data.txt
bandit12@bandit:/tmp/myans$ cd extracted_files/
bandit12@bandit:/tmp/myans/extracted_files$ ls
data5.bin
bandit12@bandit:/tmp/myans/extracted_files$ file data5.bin
data5.bin: POSIX tar archive (GNU)
bandit12@bandit:/tmp/myans/extracted_files$ mkdir new_files
bandit12@bandit:/tmp/myans/extracted_files$ tar -xvf data5.bin -C new_files/
data6.bin
bandit12@bandit:/tmp/myans/extracted_files$ cd new_files/
bandit12@bandit:/tmp/myans/extracted_files/new_files$ ls
data6.bin
bandit12@bandit:/tmp/myans/extracted_files/new_files$ file data6.bin
data6.bin: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/myans/extracted_files/new_files$ bunzip2 -c data6.bin > d4.bin
bandit12@bandit:/tmp/myans/extracted_files/new_files$ ls
d4.bin  data6.bin
bandit12@bandit:/tmp/myans/extracted_files/new_files$ file d4.bin
d4.bin: POSIX tar archive (GNU)
bandit12@bandit:/tmp/myans/extracted_files/new_files$ mkdir newnew_files
bandit12@bandit:/tmp/myans/extracted_files/new_files$ tar -xvf d4.bin -C newnew_files/
data8.bin
bandit12@bandit:/tmp/myans/extracted_files/new_files$ cd newnew_files/
bandit12@bandit:/tmp/myans/extracted_files/new_files/newnew_files$ ls
data8.bin
bandit12@bandit:/tmp/myans/extracted_files/new_files/newnew_files$ file data8.bin
data8.bin: gzip compressed data, was "data9.bin", last modified: Thu Sep 19 07:08:15 2024, max compression, from Unix, original size modulo 2^32 49
bandit12@bandit:/tmp/myans/extracted_files/new_files/newnew_files$ mv data8.bin data8.bin.gz
bandit12@bandit:/tmp/myans/extracted_files/new_files/newnew_files$ gunzip -c data8.bin.gz > d5.bin
bandit12@bandit:/tmp/myans/extracted_files/new_files/newnew_files$ file d5.bin
d5.bin: ASCII text
bandit12@bandit:/tmp/myans/extracted_files/new_files/newnew_files$ cat d5.bin
The password is FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
```
-> level 14:
```bash
bandit13@bandit:~$ ls
sshkey.private
bandit13@bandit:~$ file sshkey.private
sshkey.private: PEM RSA private key
bandit13@bandit:~$ cat sshkey.private
-----BEGIN RSA PRIVATE KEY-----
***** #此处隐藏sshkey的内容，否则无法push到github，lol
-----END RSA PRIVATE KEY-----
bandit13@bandit:~$ ls -l
total 4
-rw-r----- 1 bandit14 bandit13 1679 Sep 19 07:08 sshkey.private
bandit13@bandit:~$ ssh -i sshkey.private bandit14@localhost
The authenticity of host 'localhost (127.0.0.1)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit13/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit13/.ssh/known_hosts).

                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

!!! You are trying to log into this SSH server on port 22, which is not intended.

bandit14@localhost: Permission denied (publickey).
bandit13@bandit:~$ ssh -i sshkey.private bandit14@localhost -p 2220
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit13/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit13/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

!!! You are trying to log into this SSH server with a password on port 2220 from localhost.
!!! Connecting from localhost is blocked to conserve resources.
!!! Please log out and log in again.
```

-> level 15:
使用的是普通的TCP协议，发送信息用的是nc（netcat）
```bash
bandit14@bandit:/etc$ cd bandit_pass/
bandit14@bandit:/etc/bandit_pass$ ls
bandit0   bandit11  bandit14  bandit17  bandit2   bandit22  bandit25  bandit28  bandit30  bandit33  bandit6  bandit9
bandit1   bandit12  bandit15  bandit18  bandit20  bandit23  bandit26  bandit29  bandit31  bandit4   bandit7
bandit10  bandit13  bandit16  bandit19  bandit21  bandit24  bandit27  bandit3   bandit32  bandit5   bandit8
bandit14@bandit:/etc/bandit_pass$ cat bandit13
cat: bandit13: Permission denied
bandit14@bandit:/etc/bandit_pass$
bandit14@bandit:/etc/bandit_pass$ cat bandit14
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
bandit14@bandit:/etc/bandit_pass$
bandit14@bandit:/etc/bandit_pass$ ls -l
total 136
-r-------- 1 bandit0  bandit0   8 Sep 19 07:07 bandit0
-r-------- 1 bandit1  bandit1  33 Sep 19 07:07 bandit1
-r-------- 1 bandit10 bandit10 33 Sep 19 07:07 bandit10
-r-------- 1 bandit11 bandit11 33 Sep 19 07:07 bandit11
-r-------- 1 bandit12 bandit12 33 Sep 19 07:07 bandit12
-r-------- 1 bandit13 bandit13 33 Sep 19 07:07 bandit13
-r-------- 1 bandit14 bandit14 33 Sep 19 07:07 bandit14
-r-------- 1 bandit15 bandit15 33 Sep 19 07:07 bandit15
-r-------- 1 bandit16 bandit16 33 Sep 19 07:07 bandit16
-r-------- 1 bandit17 bandit17 33 Sep 19 07:07 bandit17
-r-------- 1 bandit18 bandit18 33 Sep 19 07:07 bandit18
-r-------- 1 bandit19 bandit19 33 Sep 19 07:07 bandit19
-r-------- 1 bandit2  bandit2  33 Sep 19 07:07 bandit2
-r-------- 1 bandit20 bandit20 33 Sep 19 07:07 bandit20
-r-------- 1 bandit21 bandit21 33 Sep 19 07:07 bandit21
-r-------- 1 bandit22 bandit22 33 Sep 19 07:07 bandit22
-r-------- 1 bandit23 bandit23 33 Sep 19 07:07 bandit23
-r-------- 1 bandit24 bandit24 33 Sep 19 07:07 bandit24
-r-------- 1 bandit25 bandit25 33 Sep 19 07:07 bandit25
-r-------- 1 bandit26 bandit26 33 Sep 19 07:08 bandit26
-r-------- 1 bandit27 bandit27 33 Sep 19 07:08 bandit27
-r-------- 1 bandit28 bandit28 33 Sep 19 07:08 bandit28
-r-------- 1 bandit29 bandit29 33 Sep 19 07:08 bandit29
-r-------- 1 bandit3  bandit3  33 Sep 19 07:08 bandit3
-r-------- 1 bandit30 bandit30 33 Sep 19 07:08 bandit30
-r-------- 1 bandit31 bandit31 33 Sep 19 07:08 bandit31
-r-------- 1 bandit32 bandit32 33 Sep 19 07:08 bandit32
-r-------- 1 bandit33 bandit33 33 Sep 19 07:08 bandit33
-r-------- 1 bandit4  bandit4  33 Sep 19 07:08 bandit4
-r-------- 1 bandit5  bandit5  33 Sep 19 07:08 bandit5
-r-------- 1 bandit6  bandit6  33 Sep 19 07:08 bandit6
-r-------- 1 bandit7  bandit7  33 Sep 19 07:08 bandit7
-r-------- 1 bandit8  bandit8  33 Sep 19 07:08 bandit8
-r-------- 1 bandit9  bandit9  33 Sep 19 07:08 bandit9
bandit14@bandit:/etc/bandit_pass$ cat bandit14
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
bandit14@bandit:/etc/bandit_pass$ echo 'MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS' | nc localhost 30000
Correct!
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo

```

-> level 16:
为SSL/TLS加密协议，不能简单使用echo和nc，需要用SSL/TLS 加密：
任务明确提到要使用 SSL/TLS 加密 来与目标服务器（localhost:30001）进行通信。
openssl s_client 正是为此类加密连接设计的工具，它会与服务器协商加密协议，确保数据的安全传输。
```bash
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = SnakeOil
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = SnakeOil
verify return:1
---
Certificate chain
 0 s:CN = SnakeOil
   i:CN = SnakeOil
   a:PKEY: rsaEncryption, 4096 (bit); sigalg: RSA-SHA256
   v:NotBefore: Jun 10 03:59:50 2024 GMT; NotAfter: Jun  8 03:59:50 2034 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIFBzCCAu+gAwIBAgIUBLz7DBxA0IfojaL/WaJzE6Sbz7cwDQYJKoZIhvcNAQEL
BQAwEzERMA8GA1UEAwwIU25ha2VPaWwwHhcNMjQwNjEwMDM1OTUwWhcNMzQwNjA4
MDM1OTUwWjATMREwDwYDVQQDDAhTbmFrZU9pbDCCAiIwDQYJKoZIhvcNAQEBBQAD
ggIPADCCAgoCggIBANI+P5QXm9Bj21FIPsQqbqZRb5XmSZZJYaam7EIJ16Fxedf+
jXAv4d/FVqiEM4BuSNsNMeBMx2Gq0lAfN33h+RMTjRoMb8yBsZsC063MLfXCk4p+
09gtGP7BS6Iy5XdmfY/fPHvA3JDEScdlDDmd6Lsbdwhv93Q8M6POVO9sv4HuS4t/
jEjr+NhE+Bjr/wDbyg7GL71BP1WPZpQnRE4OzoSrt5+bZVLvODWUFwinB0fLaGRk
GmI0r5EUOUd7HpYyoIQbiNlePGfPpHRKnmdXTTEZEoxeWWAaM1VhPGqfrB/Pnca+
vAJX7iBOb3kHinmfVOScsG/YAUR94wSELeY+UlEWJaELVUntrJ5HeRDiTChiVQ++
wnnjNbepaW6shopybUF3XXfhIb4NvwLWpvoKFXVtcVjlOujF0snVvpE+MRT0wacy
tHtjZs7Ao7GYxDz6H8AdBLKJW67uQon37a4MI260ADFMS+2vEAbNSFP+f6ii5mrB
18cY64ZaF6oU8bjGK7BArDx56bRc3WFyuBIGWAFHEuB948BcshXY7baf5jjzPmgz
mq1zdRthQB31MOM2ii6vuTkheAvKfFf+llH4M9SnES4NSF2hj9NnHga9V08wfhYc
x0W6qu+S8HUdVF+V23yTvUNgz4Q+UoGs4sHSDEsIBFqNvInnpUmtNgcR2L5PAgMB
AAGjUzBRMB0GA1UdDgQWBBTPo8kfze4P9EgxNuyk7+xDGFtAYzAfBgNVHSMEGDAW
gBTPo8kfze4P9EgxNuyk7+xDGFtAYzAPBgNVHRMBAf8EBTADAQH/MA0GCSqGSIb3
DQEBCwUAA4ICAQAKHomtmcGqyiLnhziLe97Mq2+Sul5QgYVwfx/KYOXxv2T8ZmcR
Ae9XFhZT4jsAOUDK1OXx9aZgDGJHJLNEVTe9zWv1ONFfNxEBxQgP7hhmDBWdtj6d
taqEW/Jp06X+08BtnYK9NZsvDg2YRcvOHConeMjwvEL7tQK0m+GVyQfLYg6jnrhx
egH+abucTKxabFcWSE+Vk0uJYMqcbXvB4WNKz9vj4V5Hn7/DN4xIjFko+nREw6Oa
/AUFjNnO/FPjap+d68H1LdzMH3PSs+yjGid+6Zx9FCnt9qZydW13Miqg3nDnODXw
+Z682mQFjVlGPCA5ZOQbyMKY4tNazG2n8qy2famQT3+jF8Lb6a4NGbnpeWnLMkIu
jWLWIkA9MlbdNXuajiPNVyYIK9gdoBzbfaKwoOfSsLxEqlf8rio1GGcEV5Hlz5S2
txwI0xdW9MWeGWoiLbZSbRJH4TIBFFtoBG0LoEJi0C+UPwS8CDngJB4TyrZqEld3
rH87W+Et1t/Nepoc/Eoaux9PFp5VPXP+qwQGmhir/hv7OsgBhrkYuhkjxZ8+1uk7
tUWC/XM0mpLoxsq6vVl3AJaJe1ivdA9xLytsuG4iv02Juc593HXYR8yOpow0Eq2T
U5EyeuFg5RXYwAPi7ykw1PW7zAPL4MlonEVz+QXOSx6eyhimp1VZC11SCg==
-----END CERTIFICATE-----
subject=CN = SnakeOil
issuer=CN = SnakeOil
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 2103 bytes and written 373 bytes
Verification error: self-signed certificate
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 4096 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 18 (self-signed certificate)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: B32B3CD2677C373DA29BB82EF370C62878A818E715185800A0F282A9E6B45619
    Session-ID-ctx:
    Resumption PSK: 8D8880B4FCEE29DE5B33C04DE849AB3F82437EAEF96F00C008EF8E6DCECF19378F0ECD5123FA780E8458F0F0C54DAF29
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 300 (seconds)
    TLS session ticket:
    0000 - 3d db a7 bc 36 d0 24 d5-3a 29 15 af 7e 16 ec c7   =...6.$.:)..~...
    0010 - 65 eb 0d cf 40 6c 9e c3-4b cd a4 24 ff 92 00 6e   e...@l..K..$...n
    0020 - d9 6f a8 cb f3 9f 1f 89-c4 c8 90 2c e6 e8 4a 39   .o.........,..J9
    0030 - 73 8f 7c d9 5b a4 85 5b-68 4a 0a a3 31 57 6c 59   s.|.[..[hJ..1WlY
    0040 - b5 2c e7 2f 54 6e 30 51-0b 27 ce 3a cb 79 0b cd   .,./Tn0Q.'.:.y..
    0050 - 44 8e c4 52 6f fe ab 6c-59 da d4 c0 0b 77 23 8f   D..Ro..lY....w#.
    0060 - d2 a9 40 41 39 81 31 26-65 dc fd fd 77 b0 20 cd   ..@A9.1&e...w. .
    0070 - 03 d4 9a fa 34 ac 72 9e-65 f9 8f 0d 03 7f b0 18   ....4.r.e.......
    0080 - 1a 51 32 d1 a9 d9 51 44-d0 3c 5c 3e 63 b5 59 f3   .Q2...QD.<\>c.Y.
    0090 - 59 ba 01 56 c9 bf 8b 6d-ac a0 b7 f7 c6 58 43 49   Y..V...m.....XCI
    00a0 - df c1 df 33 d3 35 b0 33-b4 46 eb 72 b9 fe b5 df   ...3.5.3.F.r....
    00b0 - 3b 7f a9 14 5e f4 47 b9-a1 9c 9d 2f eb 05 40 a9   ;...^.G..../..@.
    00c0 - 3d 4b 6a 02 ff 4f 24 8f-da d0 1b a1 cc 29 99 13   =Kj..O$......)..
    00d0 - 58 94 5d d9 1f 97 5a 9b-69 82 d1 71 8a 79 ab 47   X.]...Z.i..q.y.G

    Start Time: 1740935890
    Timeout   : 7200 (sec)
    Verify return code: 18 (self-signed certificate)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: E2122CDA0511542EE24981D23B56F7FACDD0BC31CA74B0AE4C116E10DA3F352C
    Session-ID-ctx:
    Resumption PSK: 7FF05AAC8BD5EADD4A2E4CD2354577E022E6EC5B16580C9DBB77D4DE61BB08475B65CC2CF049D1C6A9F164208A38AF32
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 300 (seconds)
    TLS session ticket:
    0000 - 3d db a7 bc 36 d0 24 d5-3a 29 15 af 7e 16 ec c7   =...6.$.:)..~...
    0010 - a7 9d 8d 8e 48 ed 60 8c-0b c6 ba 3d 36 11 ac ff   ....H.`....=6...
    0020 - cd 32 94 3f 65 22 31 66-91 0e 55 47 08 dc ed 33   .2.?e"1f..UG...3
    0030 - 13 83 89 bb 96 38 c4 21-a7 97 1d 08 3d 90 7c 09   .....8.!....=.|.
    0040 - 77 f4 1b dd ac d3 ac f0-ed b4 6f ba bc 32 11 aa   w.........o..2..
    0050 - 7c a0 9e 67 43 6b 83 ff-c9 32 7f 0e 29 bd f8 bc   |..gCk...2..)...
    0060 - 47 75 60 66 01 63 b4 94-5a c2 62 da 28 c6 d3 22   Gu`f.c..Z.b.(.."
    0070 - 84 47 32 00 eb 77 39 0d-f8 54 0d a6 39 4c 2a 07   .G2..w9..T..9L*.
    0080 - fd 84 20 52 e3 6b 4e 63-f7 dc eb 7b 3d 7e ac c9   .. R.kNc...{=~..
    0090 - ca ac 41 ba 25 68 cb a1-ea 39 d5 0b 0e bf 8c ce   ..A.%h...9......
    00a0 - ea 36 e7 8f ea aa 8d 9b-5d cc 2c 94 ca cb 5e 81   .6......].,...^.
    00b0 - a7 0a fd c8 3a cf 6d 25-36 40 87 d4 cb 72 16 2d   ....:.m%6@...r.-
    00c0 - ac ca a2 f0 86 45 34 b7-0f 1b ed 6a 5e a0 46 94   .....E4....j^.F.
    00d0 - df 0b a5 c5 27 b8 57 34-dc b1 b2 66 00 59 99 2c   ....'.W4...f.Y.,

    Start Time: 1740935890
    Timeout   : 7200 (sec)
    Verify return code: 18 (self-signed certificate)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
Correct!
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

closed
```

-> level 17:
```bash
bandit16@bandit:~$ nmap -p 31000-32000 localhost
Starting Nmap 7.94SVN ( https://nmap.org ) at 2025-03-02 17:35 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00019s latency).
Not shown: 996 closed tcp ports (conn-refused)
PORT      STATE SERVICE
31046/tcp open  unknown
31518/tcp open  unknown
31691/tcp open  unknown
31790/tcp open  unknown
31960/tcp open  unknown

Nmap done: 1 IP address (1 host up) scanned in 0.11 seconds
bandit16@bandit:~$ openssl s_client -connect localhost:31046 -quiet
4087F0F7FF7F0000:error:0A0000F4:SSL routines:ossl_statem_client_read_transition:unexpected message:../ssl/statem/statem_clnt.c:398:
bandit16@bandit:~$ openssl s_client -connect localhost:31518 -quiet
Can't use SSL_get_servername
depth=0 CN = SnakeOil
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = SnakeOil
verify return:1
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx
bandit16@bandit:~$ openssl s_client -connect localhost:31691 -quiet
4087F0F7FF7F0000:error:0A0000F4:SSL routines:ossl_statem_client_read_transition:unexpected message:../ssl/statem/statem_clnt.c:398:
bandit16@bandit:~$ openssl s_client -connect localhost:31790 -quiet
Can't use SSL_get_servername
depth=0 CN = SnakeOil
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = SnakeOil
verify return:1
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx
Correct!
-----BEGIN RSA PRIVATE KEY-----
*******
-----END RSA PRIVATE KEY-----

bandit16@bandit:/tmp$ cd /tmp
bandit16@bandit:/tmp$ echo "-----BEGIN RSA PRIVATE KEY-----
******
-----END RSA PRIVATE KEY-----" > private.key

bandit16@bandit:/tmp$ cat private.key
-----BEGIN RSA PRIVATE KEY-----
******
-----END RSA PRIVATE KEY-----
bandit16@bandit:/tmp$ ssh -i private.key bandit17@localhost
The authenticity of host 'localhost (127.0.0.1)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit16/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit16/.ssh/known_hosts).

                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

!!! You are trying to log into this SSH server on port 22, which is not intended.

bandit17@localhost: Permission denied (publickey).
bandit16@bandit:/tmp$ ssh -i private.key bandit17@localhost -p 2220
```

-> level 18:
```bash
bandit17@bandit:~$ ls
passwords.new  passwords.old
bandit17@bandit:~$ diff passwords.old passwords.new
42c42
< ktfgBvpMzWKR5ENj26IbLGSblgUG9CzB
---
> x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO

C:\Users\ink>ssh bandit18@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit18@bandit.labs.overthewire.org's password:

      ,----..            ,----,          .---.
     /   /   \         ,/   .`|         /. ./|
    /   .     :      ,`   .'  :     .--'.  ' ;
   .   /   ;.  \   ;    ;     /    /__./ \ : |
  .   ;   /  ` ; .'___,/    ,' .--'.  '   \' .
  ;   |  ; \ ; | |    :     | /___/ \ |    ' '
  |   :  | ; | ' ;    |.';  ; ;   \  \;      :
  .   |  ' ' ' : `----'  |  |  \   ;  `      |
  '   ;  \; /  |     '   :  ;   .   \    .\  ;
   \   \  ',  /      |   |  '    \   \   ' \ |
    ;   :    /       '   :  |     :   '  |--"
     \   \ .'        ;   |.'       \   \ ;
  www. `---` ver     '---' he       '---" ire.org


Welcome to OverTheWire!

If you find any problems, please report them to the #wargames channel on
discord or IRC.

--[ Playing the games ]--

  This machine might hold several wargames.
  If you are playing "somegame", then:

    * USERNAMES are somegame0, somegame1, ...
    * Most LEVELS are stored in /somegame/.
    * PASSWORDS for each level are stored in /etc/somegame_pass/.

  Write-access to homedirectories is disabled. It is advised to create a
  working directory with a hard-to-guess name in /tmp/.  You can use the
  command "mktemp -d" in order to generate a random and hard to guess
  directory in /tmp/.  Read-access to both /tmp/ is disabled and to /proc
  restricted so that users cannot snoop on eachother. Files and directories
  with easily guessable or short names will be periodically deleted! The /tmp
  directory is regularly wiped.
  Please play nice:

    * don't leave orphan processes running
    * don't leave exploit-files laying around
    * don't annoy other players
    * don't post passwords or spoilers
    * again, DONT POST SPOILERS!
      This includes writeups of your solution on your blog or website!

--[ Tips ]--

  This machine has a 64bit processor and many security-features enabled
  by default, although ASLR has been switched off.  The following
  compiler flags might be interesting:

    -m32                    compile for 32bit
    -fno-stack-protector    disable ProPolice
    -Wl,-z,norelro          disable relro

  In addition, the execstack tool can be used to flag the stack as
  executable on ELF binaries.

  Finally, network-access is limited for most levels by a local
  firewall.

--[ Tools ]--

 For your convenience we have installed a few useful tools which you can find
 in the following locations:

    * gef (https://github.com/hugsy/gef) in /opt/gef/
    * pwndbg (https://github.com/pwndbg/pwndbg) in /opt/pwndbg/
    * gdbinit (https://github.com/gdbinit/Gdbinit) in /opt/gdbinit/
    * pwntools (https://github.com/Gallopsled/pwntools)
    * radare2 (http://www.radare.org/)

--[ More information ]--

  For more information regarding individual wargames, visit
  http://www.overthewire.org/wargames/

  For support, questions or comments, contact us on discord or IRC.

  Enjoy your stay!

Byebye !
Connection to bandit.labs.overthewire.org closed.
```

-> level 19:
```bash
C:\Users\ink>ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit18@bandit.labs.overthewire.org's password:
cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8

```

-> level 20:
```bash
bandit19@bandit:~$ ls
bandit20-do
bandit19@bandit:~$ ./bandit20-do
Run a command as another user.
  Example: ./bandit20-do id
bandit19@bandit:~$ ./bandit20-do id
uid=11019(bandit19) gid=11019(bandit19) euid=11020(bandit20) groups=11019(bandit19)
bandit19@bandit:~$ ./bandit20-do cat /etc/bandit_pass/bandit20
0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
```

-> level 21:
需要打开两个终端，都登录到bandit20的ssh，在第一个终端输入：
```bash
bandit20@bandit:~$ echo "0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO" | nc -lp 12346
```
在第二个终端输入：
```bash
bandit20@bandit:~$ ./suconnect 12346
```
得到第一个终端的输出：
```bash
EeoULMCra2q0dSkYj561DX7s1CpBuOBt
```
和第二个终端的输出：
```bash
Read: 0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
Password matches, sending next password
```

>echo "GbKksEFF4yrVs6il55v6gwY5aVje5f0j" | nc -l -p 12345详细解释?

>echo "GbKksEFF4yrVs6il55v6gwY5aVje5f0j" | nc -l -p 12345 是一条组合命令，用于启动一个简单的网络监听服务，并在客户端连接时发送 bandit20 的密码。以下是详细解释：
>1. echo "GbKksEFF4yrVs6il55v6gwY5aVje5f0j"
作用：输出 bandit20 的密码（GbKksEFF4yrVs6il55v6gwY5aVje5f0j）。
解释：echo 是一个命令行工具，用于将指定的字符串输出到标准输出（通常是终端）。
在这里，echo 会输出 bandit20 的密码。
>2. |（管道）
作用：将 echo 的输出传递给下一个命令（nc）。
解释：
管道符 | 用于将一个命令的输出作为另一个命令的输入。
在这里，echo 的输出（即 bandit20 的密码）会被传递给 nc。
>3. nc -l -p 12345
作用：启动一个网络监听服务，监听本地端口 12345，并在客户端连接时发送 bandit20 的密码。
解释：
nc（Netcat）是一个强大的网络工具，可以用于创建 TCP/UDP 连接、监听端口、传输数据等。
-l：表示监听模式（listen），nc 会作为一个服务器等待客户端连接。
-p 12345：指定监听的端口号为 12345。
当客户端连接到 localhost:12345 时，nc 会将 echo 输出的内容（即 bandit20 的密码）发送给客户端。
>4. 组合命令的作用
这条命令的作用是：
启动一个监听服务，监听本地端口 12345。
当客户端连接到该端口时，nc 会将 bandit20 的密码发送给客户端。
客户端（在这里是 suconnect）会读取密码并验证是否正确。
>5. 示例流程
假设你在终端 1 中运行以下命令：
`echo "GbKksEFF4yrVs6il55v6gwY5aVje5f0j" | nc -l -p 12345`
nc 会监听端口 12345，并等待客户端连接。
在终端 2 中运行以下命令：
`./suconnect 12345`
suconnect 会连接到 localhost:12345。
nc 会将 bandit20 的密码发送给 suconnect。
suconnect 会读取密码并验证是否正确。如果正确，它会返回 bandit21 的密码。

-> level 22:
```bash
bandit21@bandit:~$ ls
bandit21@bandit:~$ cd /etc/cron.d/
bandit21@bandit:/etc/cron.d$
bandit21@bandit:/etc/cron.d$ ls
cronjob_bandit22  cronjob_bandit23  cronjob_bandit24  e2scrub_all  otw-tmp-dir  sysstat
bandit21@bandit:/etc/cron.d$ cat cronjob_bandit22
@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
bandit21@bandit:/etc/cron.d$ cat /usr/bin/cronjob_bandit22.sh
#!/bin/bash
chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
bandit21@bandit:/etc/cron.d$ cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q
```

-> level 23:
```bash
bandit22@bandit:/tmp$ cd /etc/cron.d
bandit22@bandit:/etc/cron.d$ ls
cronjob_bandit22  cronjob_bandit23  cronjob_bandit24  e2scrub_all  otw-tmp-dir  sysstat
bandit22@bandit:/etc/cron.d$ cat cronjob_bandit23
@reboot bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
* * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
bandit22@bandit:/etc/cron.d$ cat  /usr/bin/cronjob_bandit23.sh
#!/bin/bash

myname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)

echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"

cat /etc/bandit_pass/$myname > /tmp/$mytarget

bandit22@bandit:/etc/cron.d$ echo I am user bandit23 | md5sum | cut -d ' ' -f 1
8ca319486bfbbc3663ea0fbe81326349
bandit22@bandit:/etc/cron.d$ cat  /tmp/8ca319486bfbbc3663ea0fbe81326349
0Zf11ioIjMVN551jX3CmStKLYqjk54Ga
```

-> level 24:
被卡的最久的一集，我在`/tmp`中提前新建了文件夹`/tolevel24`，然后在里面`touch pw24`来存放即将得到的密码。
这里应该是需要`chmod 777 /tmp/tolevel24/pw24`的，否则后续可能密码读入不了。

接着在脚本内容的提醒下去`/var/spool/bandit24/foo`写一个`s.sh`脚本，用`vim`写方便一点。
内容就是把本关答案输入到`/tmp/tolevel24/pw24`中，要加上`chmod +x s.sh`的可执行权限。

然后就是不断刷新，因为每一分钟`foo`下的文件会执行和删除，所以当`s.sh`消失的时候就是答案显现的时候。
```bash
bandit23@bandit:/etc/cron.d$ ls
cronjob_bandit22  cronjob_bandit23  cronjob_bandit24  e2scrub_all  otw-tmp-dir  sysstat
bandit23@bandit:/etc/cron.d$ cat cronjob_bandit24
@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
bandit23@bandit:/etc/cron.d$ cat cronjob_bandit24
@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
bandit23@bandit:/etc/cron.d$ cat /usr/bin/cronjob_bandit24.sh
#!/bin/bash

myname=$(whoami)

cd /var/spool/$myname/foo
echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" ./$i)"
        if [ "${owner}" = "bandit23" ]; then
            timeout -s 9 60 ./$i
        fi
        rm -f ./$i
    fi
done

bandit23@bandit:/etc/cron.d$ cd /tmp//tolevel24
bandit23@bandit:/tmp/tolevel24$ cat pw24
bandit23@bandit:/tmp/tolevel24$ cd /var/spool/bandit24
bandit23@bandit:/var/spool/bandit24$ ls
foo
bandit23@bandit:/var/spool/bandit24$ cd foo
bandit23@bandit:/var/spool/bandit24/foo$ ls
ls: cannot open directory '.': Permission denied
bandit23@bandit:/var/spool/bandit24/foo$ vim s.sh
"s.sh" [New] 3L, 94B writtenandit24/foo$
bandit23@bandit:/var/spool/bandit24/foo$ chmod +x /var/spool/bandit24/foo/s.sh
bandit23@bandit:/var/spool/bandit24/foo$ cat s.sh
#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/tolevel24/pw24
chmod 777 /tmp/tolevel24/pw24
bandit23@bandit:/var/spool/bandit24/foo$ cat /tmp/tolevel24/pw24
bandit23@bandit:/var/spool/bandit24/foo$ cat s.sh
#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/tolevel24/pw24
chmod 777 /tmp/tolevel24/pw24
bandit23@bandit:/var/spool/bandit24/foo$ cat s.sh
#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/tolevel24/pw24
chmod 777 /tmp/tolevel24/pw24
bandit23@bandit:/var/spool/bandit24/foo$ cat s.sh
#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/tolevel24/pw24
chmod 777 /tmp/tolevel24/pw24
bandit23@bandit:/var/spool/bandit24/foo$ cat /tmp/tolevel24/pw24
bandit23@bandit:/var/spool/bandit24/foo$ cat /tmp/tolevel24/pw24
bandit23@bandit:/var/spool/bandit24/foo$ cat /tmp/tolevel24/pw24
bandit23@bandit:/var/spool/bandit24/foo$ cat s.sh
#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/tolevel24/pw24
chmod 777 /tmp/tolevel24/pw24
bandit23@bandit:/var/spool/bandit24/foo$ cat /tmp/tolevel24/pw24
bandit23@bandit:/var/spool/bandit24/foo$ cat /tmp/tolevel24/pw24
bandit23@bandit:/var/spool/bandit24/foo$ cat s.sh
#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/tolevel24/pw24
chmod 777 /tmp/tolevel24/pw24
bandit23@bandit:/var/spool/bandit24/foo$ cat /tmp/tolevel24/pw24
bandit23@bandit:/var/spool/bandit24/foo$ cat /tmp/tolevel24/pw24
bandit23@bandit:/var/spool/bandit24/foo$ cat s.sh
#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/tolevel24/pw24
chmod 777 /tmp/tolevel24/pw24
bandit23@bandit:/var/spool/bandit24/foo$ cat /tmp/tolevel24/pw24
bandit23@bandit:/var/spool/bandit24/foo$ cat /tmp/tolevel24/pw24
bandit23@bandit:/var/spool/bandit24/foo$ cat /tmp/tolevel24/pw24
bandit23@bandit:/var/spool/bandit24/foo$ cat s.sh
#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/tolevel24/pw24
chmod 777 /tmp/tolevel24/pw24
bandit23@bandit:/var/spool/bandit24/foo$ cat s.sh
#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/tolevel24/pw24
chmod 777 /tmp/tolevel24/pw24
bandit23@bandit:/var/spool/bandit24/foo$ cat /tmp/tolevel24/pw24
bandit23@bandit:/var/spool/bandit24/foo$ chmod 777 /tmp/tolevel24/pw24
bandit23@bandit:/var/spool/bandit24/foo$ cat /tmp/tolevel24/pw24
bandit23@bandit:/var/spool/bandit24/foo$ cat s.sh
cat: s.sh: No such file or directory
bandit23@bandit:/var/spool/bandit24/foo$ cat /tmp/tolevel24/pw24
gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8
```

-> level 25:
```bash

```