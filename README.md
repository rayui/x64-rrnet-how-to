# x64-rrnet-how-to

- Be on OSX
- Install Vice 2.4 from dmg, do not compile from source due to hobbled libraries
- Clone contiki from github
- Set up cartridge emulation from Inspector in Vice (apple-I)
- Install gmake from homebrew (homebrew/dupes/gmake)
- Install libpcap from homebrew (homebrew/dupes/libpcap)
- Export C1541=/Applications/Vice/tools/c1541
- edit contiki/platform/c64/contiki.main.c to use static ip address
- add the following flags to your Makefile:
* LDFLAGS = -L/usr/local/opt/libpcap/lib
* CPPFLAGS = -I/usr/local/opt/libpcap/include
- gmake disk TARGET=c64
