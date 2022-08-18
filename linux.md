- sudo apt install apt-rdepends

# نصب پکیج آفلاین
```
sudo du-sch /var/cache/apt/archive // size of folder
sudo apt clean // clear content of folder above
sudo apt install --download-only meld // download packge to folder above
sudo dpkg -i meld // install package
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
