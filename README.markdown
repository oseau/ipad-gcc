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
> rsync -avz --ignore-existing -e ssh /Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneOS5.0.sdk/usr/lib/ root@192.168.0.21:/usr/lib
> rsync -avz --ignore-existing -e ssh /Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneOS5.0.sdk/usr/include/ root@192.168.0.21:/usr/include
> rsync -avz --ignore-existing -e ssh /Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneOS5.0.sdk/System/Library/PrivateFrameworks/ root@192.168.0.21:/System/Library/PrivateFrameworks/
> rsync -avz --ignore-existing -e ssh /Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneOS5.0.sdk/System/Library/Frameworks/ root@192.168.0.21:/System/Library/Frameworks/
> scp /Developer/Platforms/iPhoneSimulator.platform/Developer/SDKs/iPhoneSimulator5.0.sdk/usr/include/crt_externs.h root@192.168.0.21:/usr/include/crt_externs.h