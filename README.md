Terminal connand to build SRB2 64bit from Ubuntu 64bit

First you have to download the windows exe file who contain the gamefiles
```
wget http://github.com/B4rabbas/Sonic-Kart/releases/download/1.0.0.0.0.0.1/srb2files.tar.gz
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
git clone https://github.com/STJr/SRB2.git
```

Go in to the folder :
```
cd SRB2
```

Start Compiling
```
export LIBGME_CFLAGS=
export LIBGME_LDFLAGS=-lgme
make -C src/ LINUX64=1
```

Copy game executable in your files folder and delete source folder & 
```
cd /..
cp ~/SRB2/bin/Linux64/Release//lsdl2srb2 ~/srb2files/
rm -rf ~/SRB2/
```
Rename and copy in /usr/games
```
sudo mv ~/srb2files/ /usr/games/SRB2/
```

Launch with :
```
/usr/games/SRB2/lsdl2srb2
```

One time copy / paste :
```
sudo apt install -y libgme-dev libsdl2-mixer-dev libsdl2-dev zlib1g-dev libpng-dev nasm build-essential git ; wget http://github.com/B4rabbas/Sonic-Kart/releases/download/1.0.0.0.0.0.1/srb2files.tar.gz ; tar xvzf srb2files.tar.gz ; rm srb2files.tar.gz ; git clone https://github.com/STJr/SRB2.git ; cd SRB2 ; export LIBGME_CFLAGS= ; export LIBGME_LDFLAGS=-lgme ; make -C src/ LINUX64=1 ; cd /.. ; cp ~/SRB2/bin/Linux64/Release//lsdl2srb2 ~/srb2files/ ; rm -rf ~/SRB2/ ; sudo mv ~/srb2files/ /usr/games/SRB2/
```











Installer version officielle de Sonic Robo Blast 2 et de Sonic Robo Blast 2 Kart sur ubuntu :

sudo apt install -y dirmngr ; sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys BC359FFF5A04B56C41DBC134289CABAB043F53A7 ; sudo add-apt-repository -y ppa:kartkrew/srb2kart ; sudo add-apt-repository -y ppa:stjr/srb2 ; sudo apt update -y ; sudo apt install -y srb2kart srb2

# SRB2Kart

[SRB2Kart](https://srb2.org/mods/) is a kart racing mod based on the 3D Sonic the Hedgehog fangame [Sonic Robo Blast 2](https://srb2.org/), based on a modified version of [Doom Legacy](http://doomlegacy.sourceforge.net/).

## Dependencies
- NASM (x86 builds only)
- SDL2 (Linux/OS X only)
- SDL2-Mixer (Linux/OS X only)
- libupnp (Linux/OS X only)
- libgme (Linux/OS X only)

## Compiling

See [SRB2 Wiki/Source code compiling](http://wiki.srb2.org/wiki/Source_code_compiling). The compiling process for SRB2Kart is largely identical to SRB2.

## Disclaimer
Kart Krew is in no way affiliated with SEGA or Sonic Team. We do not claim ownership of any of SEGA's intellectual property used in SRB2.



# Install build dependencies

sudo apt-get build-dep srb2 srb2-data

# Change to a folder of your choice, where the binary packages will be built

mkdir ~/Packages
cd ~/Packages

# Build the SRB2 package

apt source -t bionic --build srb2
apt source -t bionic --build srb2-data

# Install the SRB2 package
