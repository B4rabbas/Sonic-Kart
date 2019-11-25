You also can can download a builded version, who include a lot of mods and 3D models here :
https://github.com/B4rabbas/Sonic-Kart/releases/download/1.0.0.0.0.1/Sonic.Kart.Mania.V1.4.srb2kart

Here is a one line copy/paste to download it and install it :
```
wget https://github.com/B4rabbas/Sonic-Kart/releases/download/1.0.0.0.0.1/Sonic.Kart.Mania.V1.4.srb2kart.1.1.DEB.tar.gz ; tar xvzf Sonic.Kart.Mania.V1.3.srb2kart.1.1.DEB.tar.gz ; ~/Sonic_Kart_Mania/DATA/InstallSonicKartMania
```
read the read-me included for further informations.

# Build Sonic Robo Blast 2 64bit from Ubuntu 64bit

First you have to download the windows exe file who contain the gamefiles, but don't work with wget (idkw), here is to wget an archive from a forked repo (mine)
```
wget https://github.com/B4rabbas/Sonic-Kart/releases/download/1.0.0.0.0.0.1/sbr2kartfiles.tar.gz
```
Extract and delete archive :
```
tar xvzf srb2files.tar.gz ; rm srb2files.tar.gz
```
Dependencies :
```
sudo apt install -y libgme-dev libsdl2-mixer-dev libsdl2-dev zlib1g-dev libpng-dev nasm build-essential git
```
Download Source code :
```
git clone https://github.com/B4rabbas/Sonic-Kart.git
```
Go in to the folder :
```
cd Sonic-Kart
```
Start Compiling
```
export LIBGME_CFLAGS=
export LIBGME_LDFLAGS=-lgme
make -C src/ LINUX64=1
```
You executable is in ~/SRB2/bin/Linux64/Release/

If you want to install it, continue with

Copy game executable in your files folder and delete source folder &
```
cd /..
cp ~/Sonic-KART/bin/Linux64/Release/lsdl2srb2kart ~/sbr2kartfiles/
sudo rm -rf ~/Sonic-Kart/
```
Rename and copy in /usr/games
```
sudo mv ~/sbr2kartfiles/ /usr/games/SRB2Kart/
```
Launch with :
```
/usr/games/SRB2Kart/lsdl2srb2kart
```
One line copy past to build :
```
sudo apt install -y libgme-dev libsdl2-mixer-dev libsdl2-dev zlib1g-dev libpng-dev nasm build-essential git ; git clone https://github.com/B4rabbas/Sonic-Kart.git ; cd Sonic-Kart ; export LIBGME_CFLAGS= ; export LIBGME_LDFLAGS=-lgme ; make -C src/ LINUX64=1
```
Your compiled executable is 
~/Sonic-Kart/bin/Linux64/Release//lsdl2srb2kart

One line copy past to build and install :
```
sudo apt install -y libgme-dev libsdl2-mixer-dev libsdl2-dev zlib1g-dev libpng-dev nasm build-essential git ; wget https://github.com/B4rabbas/Sonic-Kart/releases/download/1.0.0.0.0.0.1/sbr2kartfiles.tar.gz ; tar xvzf sbr2kartfiles.tar.gz ; rm sbr2kartfiles.tar.gz ; git clone https://github.com/B4rabbas/Sonic-Kart.git ; cd Sonic-Kart ; export LIBGME_CFLAGS= ; export LIBGME_LDFLAGS=-lgme ; make -C src/ LINUX64=1 ; cd /.. ; cp ~/Sonic-KART/bin/Linux64/Release/lsdl2srb2kart ~/sbr2kartfiles/ ; sudo rm -rf ~/Sonic-Kart/ ; sudo mv ~/sbr2kartfiles/ /usr/games/SRB2Kart/
```
Launch with :
```
/usr/games/SRB2/lsdl2srb2kart
```

## Cross compilation Not tested
Compile 32 bit linux executable
```
git clone https://github.com/B4rabbas/Sonic-Kart.git
cd Sonic-Kart
export LIBGME_CFLAGS=
export LIBGME_LDFLAGS=-lgme
set PREFIX=i686-w64-mingw32
make -C src/ MINGW=1 
```

Compile 64 windows executable :
```
git clone https://github.com/B4rabbas/Sonic-Kart.git
cd Sonic-Kart
export LIBGME_CFLAGS=
export LIBGME_LDFLAGS=-lgme
set CC=gcc -m32 
make -C LINUX=1 
```
