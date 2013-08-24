# iPad Gcc
redsn0w, ipsw, iosgcc all found in **BTSync/programs/ipad** folder

##Jailbreak
 - enter DFU using reds0nw.
 - restore .ipsw in iTunes.
 - enter ReleaseMeNow
 - reboot
 - enter 'Cydia' -- 'OpenSSH Access How-To' -- 'Change Default Password'
 
##Install Gcc

- install 'apt7'(all four packages) in cydia
		
- in MobileTerminal :

		$ apt-get install uuid csu odcctools rsync
		$ apt-get install gawk make python coreutils inetutils git less
		
- upload 'iosgcc' folder to iPad (/var/root) using [Cyberduck](http://cyberduck.ch) :
		
- turn off cydia
- in MobileTerminal :

		$ cd /var/root/iosgcc
		$ dpkg -i *.deb
- test

		$ echo 'void main() { printf("Hello, world!\n"); }' > helloworld.c
		$ gcc helloworld.c -o helloworld
		$ ldid -S helloworld
		$ ./helloworld