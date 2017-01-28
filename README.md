# cjdns benchmarks

## gl-inet ar150

> 1.2 MB/s
> 6100 pkts

```bash
root@proxy:~# time cjdroute --bench && cat /proc/cpuinfo && cjdroute -v
1485582686 INFO RandomSeed.c:42 Attempting to seed random number generator
1485582686 INFO RandomSeed.c:50 Trying random seed [/dev/urandom] Success
1485582686 INFO RandomSeed.c:50 Trying random seed [/proc/sys/kernel/random/uuid (Linux)] Success
1485582686 INFO RandomSeed.c:50 Trying random seed [getentropy(2)] Success
1485582686 INFO RandomSeed.c:64 Seeding random number generator succeeded with [3] sources
1485582686 INFO Benchmark.c:71 Setting up salsa20/poly1305 benchmark (encryption and decryption only)
1485582686 DEBUG CryptoAuth.c:393 0x56162354 bench [7a54:2039:cf3a:7c74:7376:1597:ebc7:cf12]: Sending hello packet
1485582686 DEBUG CryptoAuth.c:589 0x561624c4 bench [83cd:d52e:f9bb:cb49:b97a:8ac2:ae4a:dffd]: Received a hello packet, using auth: 0
1485582686 DEBUG CryptoAuth.c:393 0x561624c4 bench [83cd:d52e:f9bb:cb49:b97a:8ac2:ae4a:dffd]: Sending key packet
1485582686 DEBUG CryptoAuth.c:602 0x56162354 bench [7a54:2039:cf3a:7c74:7376:1597:ebc7:cf12]: Received a key packet
1485582686 DEBUG CryptoAuth.c:485 0x56162354 bench [7a54:2039:cf3a:7c74:7376:1597:ebc7:cf12]: Doing final step to send message. nonce=4
1485582686 DEBUG CryptoAuth.c:791 0x561624c4 bench [83cd:d52e:f9bb:cb49:b97a:8ac2:ae4a:dffd]: Trying final handshake step, nonce=4
1485582686 DEBUG CryptoAuth.c:802 0x561624c4 bench [83cd:d52e:f9bb:cb49:b97a:8ac2:ae4a:dffd]: Final handshake step succeeded
1485582686 DEBUG CryptoAuth.c:791 0x56162354 bench [7a54:2039:cf3a:7c74:7376:1597:ebc7:cf12]: Trying final handshake step, nonce=6
1485582686 DEBUG CryptoAuth.c:802 0x56162354 bench [7a54:2039:cf3a:7c74:7376:1597:ebc7:cf12]: Final handshake step succeeded
1485582686 INFO Benchmark.c:47 ----- Begin salsa20/poly1305 benchmark -----
1485582808 INFO Benchmark.c:59  
1485582808 INFO Benchmark.c:60 ---------------------------------------------------------------
1485582808 INFO Benchmark.c:62 Benchmark salsa20/poly1305 in 122113ms. 9826 kilobits per second
1485582808 INFO Benchmark.c:63 ---------------------------------------------------------------
1485582808 INFO Benchmark.c:64  
1485582808 INFO Benchmark.c:149 Setting up salsa20/poly1305 benchmark (encryption and decryption only)
1485582808 DEBUG InterfaceController.c:826 bootstrapPeer total [0]
1485582808 INFO InterfaceController.c:877 Adding peer [v0.0000.0000.0000.0013.kmzm4w0kj9bswd5qmx74nu7kusv5pj40vcsmp781j6xxgpd59z00.k] from bootstrapPeer()
1485582808 DEBUG InterfaceController.c:286 SwitchPing [kmzm4w0kj9bswd5qmx74nu7kusv5pj40vcsmp781j6xxgpd59z00.k]
1485582808 DEBUG CryptoAuth.c:393 0x562555a4 outer [fc41:94b5:0925:7ba9:3959:11ab:a006:367a]: Sending hello packet
1485582808 DEBUG CryptoAuth.c:589 0x562572b4 outer [fc1f:5b96:e1c5:625d:afde:2523:a7fa:383a]: Received a hello packet, using auth: 1
1485582808 INFO InterfaceController.c:662 Added peer [v0.0000.0000.0000.0013.vz21tg07061s8v9mckrvgtfds7j2u5lst8cwl6nqhp81njrh5wg0.k] from incoming message
1485582808 DEBUG InterfaceController.c:286 SwitchPing [vz21tg07061s8v9mckrvgtfds7j2u5lst8cwl6nqhp81njrh5wg0.k]
1485582808 DEBUG ControlHandler.c:151 ctrl packet from [0000.0000.0000.0013]
1485582808 DEBUG ControlHandler.c:101 got switch ping from [0000.0000.0000.0013]
1485582808 DEBUG CryptoAuth.c:393 0x562572b4 outer [fc1f:5b96:e1c5:625d:afde:2523:a7fa:383a]: Sending key packet
1485582808 DEBUG CryptoAuth.c:602 0x562555a4 outer [fc41:94b5:0925:7ba9:3959:11ab:a006:367a]: Received a key packet
1485582808 DEBUG InterfaceController.c:286 SwitchPing [kmzm4w0kj9bswd5qmx74nu7kusv5pj40vcsmp781j6xxgpd59z00.k]
1485582808 DEBUG CryptoAuth.c:485 0x562555a4 outer [fc41:94b5:0925:7ba9:3959:11ab:a006:367a]: Doing final step to send message. nonce=4
1485582808 DEBUG CryptoAuth.c:791 0x562572b4 outer [fc1f:5b96:e1c5:625d:afde:2523:a7fa:383a]: Trying final handshake step, nonce=4
1485582808 DEBUG CryptoAuth.c:802 0x562572b4 outer [fc1f:5b96:e1c5:625d:afde:2523:a7fa:383a]: Final handshake step succeeded
1485582808 DEBUG InterfaceController.c:379 Checking for old sessions to merge with.
1485582808 DEBUG ControlHandler.c:151 ctrl packet from [0000.0000.0000.0013]
1485582808 DEBUG ControlHandler.c:101 got switch ping from [0000.0000.0000.0013]
1485582808 DEBUG CryptoAuth.c:791 0x562555a4 outer [fc41:94b5:0925:7ba9:3959:11ab:a006:367a]: Trying final handshake step, nonce=6
1485582808 DEBUG CryptoAuth.c:802 0x562555a4 outer [fc41:94b5:0925:7ba9:3959:11ab:a006:367a]: Final handshake step succeeded
1485582808 DEBUG InterfaceController.c:379 Checking for old sessions to merge with.
1485582808 DEBUG ControlHandler.c:151 ctrl packet from [0000.0000.0000.0013]
1485582808 DEBUG ControlHandler.c:101 got switch ping from [0000.0000.0000.0013]
1485582808 DEBUG ControlHandler.c:151 ctrl packet from [0000.0000.0000.0013]
1485582808 DEBUG ControlHandler.c:101 got switch ping from [0000.0000.0000.0013]
1485582808 DEBUG ControlHandler.c:151 ctrl packet from [0000.0000.0000.0013]
1485582808 DEBUG ControlHandler.c:101 got switch ping from [0000.0000.0000.0013]
1485582808 INFO Benchmark.c:47 ----- Begin Switching benchmark -----
1485582976 INFO Benchmark.c:59  
1485582976 INFO Benchmark.c:60 ---------------------------------------------------------------
1485582976 INFO Benchmark.c:62 Benchmark Switching in 167847ms. 6100 packets per second
1485582976 INFO Benchmark.c:63 ---------------------------------------------------------------
1485582976 INFO Benchmark.c:64  
1485582976 INFO Benchmark.c:221 DONE
real    4m 50.48s
user    3m 46.72s
sys     0m 8.70s
system type             : Atheros AR9330 rev 1
machine                 : GL AR150
processor               : 0
cpu model               : MIPS 24Kc V7.4
BogoMIPS                : 265.42
wait instruction        : yes
microsecond timers      : yes
tlb_entries             : 16
extra interrupt vector  : yes
hardware watchpoint     : yes, count: 4, address/irw mask: [0x0ffc, 0x0ffc, 0x0ffb, 0x0ffb]
isa                     : mips1 mips2 mips32r1 mips32r2
ASEs implemented        : mips16
shadow register sets    : 1
kscratch registers      : 0
package                 : 0
core                    : 0
VCED exceptions         : not available
VCEI exceptions         : not available

Cjdns version: 40e87d9419c19063e772e39c7c59a8a8771c5ee8
Cjdns protocol version: 18
```

## macbook pro 2015

> 146.3 MB/s
> 502,453 pkts

```bash
bash-3.2$ time cjdroute --bench && sysctl -n machdep.cpu.brand_string && brew info cjdns | head -6 && cjdroute -v
1485583828 INFO RandomSeed.c:42 Attempting to seed random number generator
1485583828 INFO RandomSeed.c:50 Trying random seed [/dev/urandom] Success
1485583828 INFO RandomSeed.c:64 Seeding random number generator succeeded with [1] sources
1485583828 INFO Benchmark.c:71 Setting up salsa20/poly1305 benchmark (encryption and decryption only)
1485583828 DEBUG CryptoAuth.c:393 0x7feb65d0bc78 bench [0671:5aac:7cb2:ab7d:5070:75e1:00c2:015f]: Sending hello packet
1485583828 DEBUG CryptoAuth.c:589 0x7feb65d0be38 bench [c9e6:31bb:4ace:3fc2:6ff2:3ee6:c649:d4d7]: Received a hello packet, using auth: 0
1485583828 DEBUG CryptoAuth.c:393 0x7feb65d0be38 bench [c9e6:31bb:4ace:3fc2:6ff2:3ee6:c649:d4d7]: Sending key packet
1485583828 DEBUG CryptoAuth.c:602 0x7feb65d0bc78 bench [0671:5aac:7cb2:ab7d:5070:75e1:00c2:015f]: Received a key packet
1485583828 DEBUG CryptoAuth.c:485 0x7feb65d0bc78 bench [0671:5aac:7cb2:ab7d:5070:75e1:00c2:015f]: Doing final step to send message. nonce=4
1485583828 DEBUG CryptoAuth.c:791 0x7feb65d0be38 bench [c9e6:31bb:4ace:3fc2:6ff2:3ee6:c649:d4d7]: Trying final handshake step, nonce=4
1485583828 DEBUG CryptoAuth.c:802 0x7feb65d0be38 bench [c9e6:31bb:4ace:3fc2:6ff2:3ee6:c649:d4d7]: Final handshake step succeeded
1485583828 DEBUG CryptoAuth.c:791 0x7feb65d0bc78 bench [0671:5aac:7cb2:ab7d:5070:75e1:00c2:015f]: Trying final handshake step, nonce=6
1485583828 DEBUG CryptoAuth.c:802 0x7feb65d0bc78 bench [0671:5aac:7cb2:ab7d:5070:75e1:00c2:015f]: Final handshake step succeeded
1485583828 INFO Benchmark.c:47 ----- Begin salsa20/poly1305 benchmark -----
1485583829 INFO Benchmark.c:59  
1485583829 INFO Benchmark.c:60 ---------------------------------------------------------------
1485583829 INFO Benchmark.c:62 Benchmark salsa20/poly1305 in 1025ms. 1170731 kilobits per second
1485583829 INFO Benchmark.c:63 ---------------------------------------------------------------
1485583829 INFO Benchmark.c:64  
1485583829 INFO Benchmark.c:149 Setting up salsa20/poly1305 benchmark (encryption and decryption only)
1485583829 DEBUG InterfaceController.c:829 bootstrapPeer total [0]
1485583829 INFO InterfaceController.c:880 Adding peer [v0.0000.0000.0000.0013.kmzm4w0kj9bswd5qmx74nu7kusv5pj40vcsmp781j6xxgpd59z00.k] from bootstrapPeer()
1485583829 DEBUG InterfaceController.c:289 SwitchPing [kmzm4w0kj9bswd5qmx74nu7kusv5pj40vcsmp781j6xxgpd59z00.k]
1485583829 DEBUG CryptoAuth.c:393 0x7feb65c03fb8 outer [fc41:94b5:0925:7ba9:3959:11ab:a006:367a]: Sending hello packet
1485583829 DEBUG CryptoAuth.c:589 0x7feb65e00748 outer [fc1f:5b96:e1c5:625d:afde:2523:a7fa:383a]: Received a hello packet, using auth: 1
1485583829 INFO InterfaceController.c:665 Added peer [v0.0000.0000.0000.0013.vz21tg07061s8v9mckrvgtfds7j2u5lst8cwl6nqhp81njrh5wg0.k] from incoming message
1485583829 DEBUG InterfaceController.c:289 SwitchPing [vz21tg07061s8v9mckrvgtfds7j2u5lst8cwl6nqhp81njrh5wg0.k]
1485583829 DEBUG ControlHandler.c:150 ctrl packet from [0000.0000.0000.0013]
1485583829 DEBUG ControlHandler.c:100 got switch ping from [0000.0000.0000.0013]
1485583829 DEBUG CryptoAuth.c:393 0x7feb65e00748 outer [fc1f:5b96:e1c5:625d:afde:2523:a7fa:383a]: Sending key packet
1485583829 DEBUG CryptoAuth.c:602 0x7feb65c03fb8 outer [fc41:94b5:0925:7ba9:3959:11ab:a006:367a]: Received a key packet
1485583829 DEBUG InterfaceController.c:289 SwitchPing [kmzm4w0kj9bswd5qmx74nu7kusv5pj40vcsmp781j6xxgpd59z00.k]
1485583829 DEBUG CryptoAuth.c:485 0x7feb65c03fb8 outer [fc41:94b5:0925:7ba9:3959:11ab:a006:367a]: Doing final step to send message. nonce=4
1485583829 DEBUG CryptoAuth.c:791 0x7feb65e00748 outer [fc1f:5b96:e1c5:625d:afde:2523:a7fa:383a]: Trying final handshake step, nonce=4
1485583829 DEBUG CryptoAuth.c:802 0x7feb65e00748 outer [fc1f:5b96:e1c5:625d:afde:2523:a7fa:383a]: Final handshake step succeeded
1485583829 DEBUG InterfaceController.c:382 Checking for old sessions to merge with.
1485583829 DEBUG ControlHandler.c:150 ctrl packet from [0000.0000.0000.0013]
1485583829 DEBUG ControlHandler.c:100 got switch ping from [0000.0000.0000.0013]
1485583829 DEBUG CryptoAuth.c:791 0x7feb65c03fb8 outer [fc41:94b5:0925:7ba9:3959:11ab:a006:367a]: Trying final handshake step, nonce=6
1485583829 DEBUG CryptoAuth.c:802 0x7feb65c03fb8 outer [fc41:94b5:0925:7ba9:3959:11ab:a006:367a]: Final handshake step succeeded
1485583829 DEBUG InterfaceController.c:382 Checking for old sessions to merge with.
1485583829 DEBUG ControlHandler.c:150 ctrl packet from [0000.0000.0000.0013]
1485583829 DEBUG ControlHandler.c:100 got switch ping from [0000.0000.0000.0013]
1485583829 DEBUG ControlHandler.c:150 ctrl packet from [0000.0000.0000.0013]
1485583829 DEBUG ControlHandler.c:100 got switch ping from [0000.0000.0000.0013]
1485583829 DEBUG ControlHandler.c:150 ctrl packet from [0000.0000.0000.0013]
1485583829 DEBUG ControlHandler.c:100 got switch ping from [0000.0000.0000.0013]
1485583829 INFO Benchmark.c:47 ----- Begin Switching benchmark -----
1485583831 INFO Benchmark.c:59  
1485583831 INFO Benchmark.c:60 ---------------------------------------------------------------
1485583831 INFO Benchmark.c:62 Benchmark Switching in 2038ms. 502453 packets per second
1485583831 INFO Benchmark.c:63 ---------------------------------------------------------------
1485583831 INFO Benchmark.c:64  
1485583831 INFO Benchmark.c:221 DONE

real    0m3.076s
user    0m2.902s
sys     0m0.020s
Intel(R) Core(TM) i5-5257U CPU @ 2.70GHz
cjdns: stable 18 (bottled), HEAD
Advanced mesh routing system with cryptographic addressing
https://github.com/cjdelisle/cjdns/
/usr/local/Cellar/cjdns/18 (6 files, 1.6M) *
  Poured from bottle on 2017-01-20 at 22:18:07
From: https://github.com/Homebrew/homebrew-core/blob/master/Formula/cjdns.rb
Cjdns version: unknown
Cjdns protocol version: 18
```
