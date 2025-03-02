level 0:

ssh bandit0@bandit.labs.overthewire.org -p 2220

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

->level 3:

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

