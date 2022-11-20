# Usful Commands
`apt show package-name` -> show information and description :)

---

- sudo apt install apt-rdepends

# نصب پکیج آفلاین
```
sudo du-sch /var/cache/apt/archive // size of folder
sudo apt clean // clear content of folder above
sudo apt install --download-only meld // download packge to folder above
sudo dpkg -i meld // install package
```
# Install Offline package `NEW`
we have two pc: `online` and `offline`
1. copy packages list in `online`
```
sudo apt update
cp /var/lib/apt/lists/* ~/off/list
```
2. download package in `online`
```
sudo apt install --download-only smbclient
ls /var/cache/apt/archives/
sudo cp /var/cache/apt/archives/*.deb ~/off/pack
```
3. update package list `offline`
```
cp ~/off/list/* /var/lib/apt/lists/
sudo apt-get dist-upgrade
```
#### NOTE: in command `dist-upgrade` select `n` to cancel command, this command update packge list!!!
4. install package in `offline`
```
sudo cp ~/off/pack/* /var/cache/apt/archives/
sudo apt install smbclient
```
# View list shared folders
#### NOTE: Replace ALL `[xxxxx]`
1. List shared folders
```
smbclient -L //192.168.1.1 -U [DOMAIN]/[username]
```
2. go to share folder
```
smbclient //192.168.1.1/[folder name] -U [DOMAIN]/[username]
```


# Run only the Linux kernel and user programs
https://unix.stackexchange.com/questions/175386/run-only-the-linux-kernel-and-user-programs

- https://0xax.gitbooks.io/linux-insides/content/

# Serial linux
https://www.freebsd.org/doc/en/articles/serial-uart/index.html

http://man7.org/linux/man-pages/man3/tcsetattr.3.html

https://en.wikibooks.org/wiki/Serial_Programming/termios

http://www.tldp.org/HOWTO/Serial-Programming-HOWTO/x115.html

http://linux.die.net/man/3/termios

https://www.cmrr.umn.edu/~strupp/serial.html

https://blog.nelhage.com/2009/12/a-brief-introduction-to-termios-termios3-and-stty/

http://stackoverflow.com/questions/6947413/how-to-open-read-and-write-from-serial-port-in-c

http://www.unixwiz.net/techtips/termios-vmin-vtime.html

http://www.comptechdoc.org/os/linux/programming/c/linux_pgcserial.html

# Share folder
- command line: smbclient: https://www.chrisrmiller.com/mount-samba-share-in-ubuntu/
- working with smbclient: https://www.computerhope.com/issues/ch001636.htm
- mount: cifs: https://www.ceos3c.com/linux/mount-cifs-permission-denied-linux/
