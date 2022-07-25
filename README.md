# dev-container-mac-issue

Dev Container is run with CPU op-mode 32-bit on Mac OS/M1.

# Issue

If you open this project on VS Code on a local dev container in a Mac Os X machine with M1, and open a terminal, you get this when you run ´lscpu´:

```
root ➜ /workspaces/dev-container-mac-issue (main ✗) $ lscpu
Architecture:        x86_64
CPU op-mode(s):      32-bit
Byte Order:          Little Endian
CPU(s):              4
On-line CPU(s) list: 0-3
Thread(s) per core:  1
Core(s) per socket:  4
Socket(s):           1
Vendor ID:           0x00
Model:               0
Stepping:            0x0
BogoMIPS:            48.00
Flags:               fp asimd evtstrm aes pmull sha1 sha2 crc32 atomics fphp asimdhp cpuid asimdrdm jscvt fcma lrcpc dcpop sha3 asimddp sha512 asimdfhm dit uscat ilrcpc flagm sb paca pacg dcpodp flagm2 frint
```

Notice that the CPU op-mode is 32-bit even though the architecture is x86_64.