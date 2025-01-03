# postal-psp
PSP port of Postal 

![image](https://github.com/user-attachments/assets/46afc14a-58c4-4cf2-81a2-8ddb0a5c698e)

This is a port of the [original Postal source code](https://github.com/RWS-Studios/POSTAL-SourceCode) for Sony PSP

Toolchain is [PSPDEV](https://pspdev.github.io/installation.html)

To play get a copy at [Steam](https://store.steampowered.com/app/232770/POSTAL/) or [GOG](https://www.gog.com/en/game/postal_classic_and_uncut)

## Buildung

After setting up PSPDEV and git clone the repo
```bash
cd postal-psp
mkdir build && cd build
psp-cmake -DBUILD_PRX=1 -DENC_PRX=1 .. && make
cd build
make
```

## Known issues

- Plays fine in PPSSPP but crashes on real hardware
-  Low fps (high cpu usage)