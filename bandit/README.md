# 0
```
❯ ssh bandit0@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _   
                        | |__   __ _ _ __   __| (_) |_ 
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_ 
                        |_.__/ \__,_|_| |_|\__,_|_|\__|
                                                       

                      This is an OverTheWire game server. 
            More information on http://www.overthewire.org/wargames

bandit0@bandit.labs.overthewire.org's password: 

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
    * peda (https://github.com/longld/peda.git) in /opt/peda/
    * gdbinit (https://github.com/gdbinit/Gdbinit) in /opt/gdbinit/
    * pwntools (https://github.com/Gallopsled/pwntools)
    * radare2 (http://www.radare.org/)

 Both python2 and python3 are installed.

--[ More information ]--

  For more information regarding individual wargames, visit
  http://www.overthewire.org/wargames/

  For support, questions or comments, contact us on discord or IRC.

  Enjoy your stay!

bandit0@bandit:~$ ls
readme
bandit0@bandit:~$ cat readme
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
```
# 1
```
❯ ssh bandit1@bandit.labs.overthewire.org -p 2220
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
```
# 2
```
❯ ssh bandit2@bandit.labs.overthewire.org -p 2220
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat spaces\ in\ this\ filename 
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
```
# 3
```
❯ ssh bandit3@bandit.labs.overthewire.org -p 2220
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cat inhere/.hidden 
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
```
# 4
```
❯ ssh bandit4@bandit.labs.overthewire.org -p 2220
bandit4@bandit:~$ ls
inhere
bandit4@bandit:~$ cd inhere/
bandit4@bandit:~/inhere$ ls
-file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09
bandit4@bandit:~/inhere$ file ./*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: Non-ISO extended-ASCII text, with no line terminators
bandit4@bandit:~/inhere$ cat ./-file07
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
```
# 5
```
❯ ssh bandit5@bandit.labs.overthewire.org -p 2220
bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere/
bandit5@bandit:~/inhere$ ls
maybehere00  maybehere03  maybehere06  maybehere09  maybehere12  maybehere15  maybehere18
maybehere01  maybehere04  maybehere07  maybehere10  maybehere13  maybehere16  maybehere19
maybehere02  maybehere05  maybehere08  maybehere11  maybehere14  maybehere17
bandit5@bandit:~/inhere$ find . -size 1033c               
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2         
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
```
# 6
```
❯ ssh bandit6@bandit.labs.overthewire.org -p 2220
bandit6@bandit:~$ ls
bandit6@bandit:~$ find / -user bandit7 -group bandit6 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password 
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
```
# 7
```
❯ ssh bandit7@bandit.labs.overthewire.org -p 2220
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ cat data.txt | grep millionth
millionth	TESKZC0XvTetK0S9xNwm25STk5iWrBvP
```
# 8
```
❯ ssh bandit8@bandit.labs.overthewire.org -p 2220
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ cat data.txt | sort | uniq -c | grep '1 '   
      1 EN632PlfYiZbn3PhVK3XOGSlNInNE00t
```
# 9
```
❯ ssh bandit9@bandit.labs.overthewire.org -p 2220
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ strings data.txt | grep ==
4========== the#
========== password
========== is
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```
# 10
```
❯ ssh bandit10@bandit.labs.overthewire.org -p 2220
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt 
VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
bandit10@bandit:~$ base64 -d data.txt 
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
```
# 11
```
❯ ssh bandit11@bandit.labs.overthewire.org -p 2220
bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ cat data.txt 
Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi
bandit11@bandit:~$ cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
```
# 12
```
❯ ssh bandit12@bandit.labs.overthewire.org -p 2220
bandit12@bandit:~$ ls
data.txt
bandit12@bandit:~$ mkdir /tmp/stuff
bandit12@bandit:~$ cp data.txt /tmp/stuff
bandit12@bandit:~$ cd /tmp/stuff
bandit12@bandit:/tmp/stuff$ cat data.txt 
00000000: 1f8b 0808 2773 4564 0203 6461 7461 322e  ....'sEd..data2.
...
bandit12@bandit:/tmp/stuff$ xxd -r data.txt binary.gz
bandit12@bandit:/tmp/stuff$ gzip -d binary.gz
bandit12@bandit:/tmp/stuff$ xxd binary 
00000000: 425a 6839 3141 5926 5359 7b4f 965f 0000  BZh91AY&SY{O._..
...
bandit12@bandit:/tmp/stuff$ bzip2 -d binary
bzip2: Can't guess original name for binary -- using binary.out
bandit12@bandit:/tmp/stuff$ xxd binary.out 
00000000: 1f8b 0808 2773 4564 0203 6461 7461 342e  ....'sEd..data4.
...
bandit12@bandit:/tmp/stuff$ mv binary.out binary.gz
bandit12@bandit:/tmp/stuff$ gzip -d binary.gz
bandit12@bandit:/tmp/stuff$ xxd binary | head      
00000000: 6461 7461 352e 6269 6e00 0000 0000 0000  data5.bin.......
...
bandit12@bandit:/tmp/stuff$ tar -xf binary   
bandit12@bandit:/tmp/stuff$ ls
binary  data5.bin  data.txt
bandit12@bandit:/tmp/stuff$ xxd data5.bin | head
00000000: 6461 7461 362e 6269 6e00 0000 0000 0000  data6.bin.......
...
bandit12@bandit:/tmp/stuff$ tar -xf data5.bin
bandit12@bandit:/tmp/stuff$ xxd data6.bin
00000000: 425a 6839 3141 5926 5359 4911 0aa4 0000  BZh91AY&SYI.....
...
bandit12@bandit:/tmp/stuff$ bzip2 -d data6.bin
bzip2: Can't guess original name for data6.bin -- using data6.bin.out
bandit12@bandit:/tmp/stuff$ xxd data6.bin.out | head
00000000: 6461 7461 382e 6269 6e00 0000 0000 0000  data8.bin.......
...
bandit12@bandit:/tmp/stuff$ tar -xf data6.bin.out 
bandit12@bandit:/tmp/stuff$ ls
binary  data5.bin  data6.bin.out  data8.bin  data.txt
bandit12@bandit:/tmp/stuff$ xxd data8.bin 
00000000: 1f8b 0808 2773 4564 0203 6461 7461 392e  ....'sEd..data9.
...
bandit12@bandit:/tmp/stuff$ mv data8.bin data.gz
bandit12@bandit:/tmp/stuff$ gzip -d data.gz
bandit12@bandit:/tmp/stuff$ cat data
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
```
# 13
```
❯ ssh bandit13@bandit.labs.overthewire.org -p 2220
bandit13@bandit:~$ ls
sshkey.private
bandit13@bandit:~$ exit
logout
Connection to bandit.labs.overthewire.org closed.
❯ scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private .
                         _                     _ _ _   
                        | |__   __ _ _ __   __| (_) |_ 
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_ 
                        |_.__/ \__,_|_| |_|\__,_|_|\__|
                                                       

                      This is an OverTheWire game server. 
            More information on http://www.overthewire.org/wargames

bandit13@bandit.labs.overthewire.org's password: 
sshkey.private                                                                100% 1679     7.7KB/s   00:00
❯ chmod 0400 sshkey.private
```
# 14
```
❯ ssh bandit14@bandit.labs.overthewire.org -p 2220 -i sshkey.private
bandit14@bandit:~$  cat /etc/bandit_pass/bandit14
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
bandit14@bandit:~$ nc localhost 30000
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
```