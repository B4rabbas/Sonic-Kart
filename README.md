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
sudo rm -rf ~/SRB2/
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
sudo apt install -y libgme-dev libsdl2-mixer-dev libsdl2-dev zlib1g-dev libpng-dev nasm build-essential git ; wget http://github.com/B4rabbas/Sonic-Kart/releases/download/1.0.0.0.0.0.1/srb2files.tar.gz ; tar xvzf srb2files.tar.gz ; rm srb2files.tar.gz ; git clone https://github.com/STJr/SRB2.git ; cd SRB2 ; export LIBGME_CFLAGS= ; export LIBGME_LDFLAGS=-lgme ; make -C src/ LINUX64=1 ; cd /.. ; cp ~/SRB2/bin/Linux64/Release//lsdl2srb2 ~/srb2files/ ; sudo rm -rf ~/SRB2/ ; sudo mv ~/srb2files/ /usr/games/SRB2/
```



Terminal connand to build SRB2Kart 64bit from Ubuntu 64bit

First you have to download the windows exe file who contain the gamefiles
```
wget https://github.com/B4rabbas/Sonic-Kart/releases/download/1.0.0.0.0.0.1/sbr2kartfiles.tar.gz
```

Extract and delete archive :
```
tar xvzf sbr2kartfiles.tar.gz ; rm sbr2kartfiles.tar.gz
```

Dependencies :
```
sudo apt install -y libgme-dev libsdl2-mixer-dev libsdl2-dev zlib1g-dev libpng-dev nasm build-essential git
```

Download Source code :
```
git clone https://github.com/STJr/Kart-Public.git
```

Go in to the folder :
```
cd Kart-Public
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
cp ~/Kart-Public/bin/Linux64/Release/lsdl2srb2kart ~/sbr2kartfiles/
sudo rm -rf ~/Kart-Public/
```
Rename and copy in /usr/games
```
sudo mv ~/sbr2kartfiles/ /usr/games/SRB2Kart/
```

Launch with :
```
/usr/games/SRB2Kart/lsdl2srb2kart
```

One time copy / paste :
```
sudo apt install -y libgme-dev libsdl2-mixer-dev libsdl2-dev zlib1g-dev libpng-dev nasm build-essential git ; wget https://github.com/B4rabbas/Sonic-Kart/releases/download/1.0.0.0.0.0.1/sbr2kartfiles.tar.gz ; tar xvzf sbr2kartfiles.tar.gz ; rm sbr2kartfiles.tar.gz ; git clone https://github.com/STJr/Kart-Public.git ; cd Kart-Public ; export LIBGME_CFLAGS= ; export LIBGME_LDFLAGS=-lgme ; make -C src/ LINUX64=1 ; cd /.. ; cp ~/Kart-Public/bin/Linux64/Release/lsdl2srb2kart ~/sbr2kartfiles/ ; sudo rm -rf ~/Kart-Public/ ; sudo mv ~/sbr2kartfiles/ /usr/games/SRB2Kart/
...





Install Sonic Robo Blast 2 & de Sonic Robo Blast 2 Kart sur ubuntu :

sudo apt install -y dirmngr ; sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys BC359FFF5A04B56C41DBC134289CABAB043F53A7 ; sudo add-apt-repository -y ppa:kartkrew/srb2kart ; sudo add-apt-repository -y ppa:stjr/srb2 ; sudo apt update -y ; sudo apt install -y srb2kart srb2


