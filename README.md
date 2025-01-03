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
psp-cmake -DBUILD_PRX=1 .. 
make
```

#### DO NOT USE `-DENC_PRX=1`  

### Debbuging using WSL

- Open Windows PowerShell as admin and install `winget install usbipd` 
- Then usbipd list and look for PSP Type-B
- usbipd attach --wsl --busid=X-X
- Then run [PSP Link](https://pspdev.github.io/debugging.html)

## Known issues

- Plays fine in PPSSPP but slow and unstable on real hardware
- Low FPS (high cpu usage)
- Long loading times
- Controls need to be adjusted