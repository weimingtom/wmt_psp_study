# wmt_psp_study
My PSP homebrew software study

## PSPSDK  
* https://pspdev.github.io/pspsdk/  
* https://github.com/pspdev/pspsdk/blob/master/src/samples/gu/cube/cube.c
* https://github.com/pspdev/pspsdk/blob/master/src/samples/template/elf_template/main.c
* https://sourceforge.net/projects/minpspw
* https://github.com/weimingtom/wmt_psp_study/blob/master/pspdev_001.txt  
see also https://pspdev.github.io/installation/ubuntu.html  
**Don't need to git clone pspdev and psptoolchain, just wget releases tar.gz**   
https://github.com/pspdev/pspdev/releases/tag/v20200623  
**If use Xubuntu 20.04, need to wget oldest file**  
**If use Xubuntu 20.04, need to git checkout -f 3cfacc6 for pspdev src samples**  
```
$ sudo apt-get update
$ sudo apt-get install build-essential cmake pkgconf libreadline8 libusb-0.1 libgpgme11 libarchive-tools fakeroot
$ gedit ~/.bashrc
(adding lines to .bashrc file end
export PSPDEV="$HOME/pspdev"
export PATH="$PATH:$PSPDEV/bin"
)

(v20200623 is good for xubuntu 20.04)
$ wget https://github.com/pspdev/pspdev/releases/download/v20200623/pspdev-ubuntu-latest.tar.gz
$ tar xzf pspdev-ubuntu-latest.tar.gz
$ source ~/.bashrc
$ psp-config --pspdev-path
/home/wmt/pspdev
$ psp-gcc -v
Using built-in specs.
COLLECT_GCC=psp-gcc
COLLECT_LTO_WRAPPER=/home/wmt/pspdev/bin/../libexec/gcc/psp/9.3.0/lto-wrapper
Target: psp
Configured with: ../configure --prefix=/home/runner/work/pspdev/pspdev/pspdev --target=psp --enable-languages=c,c++ --enable-lto --with-newlib --enable-cxx-flags=-G0
Thread model: single
gcc version 9.3.0 (GCC) 

$ git clone https://github.com/pspdev/pspsdk
$ cd pspsdk
$ git checkout -f 3cfacc6
$ cd src/samples/gu/cube
$ make -f Makefile.sample clean
$ make -f Makefile.sample
$ ls
cube.c    cube.o     logo.o    Makefile.sample
cube.elf  EBOOT.PBP  logo.raw  PARAM.SFO
$ /home/wmt/work_ppsspp/ppsspp/build/PPSSPPSDL
(if want to cmake PPSSPPSDL, need to 'git submodule update --init --recursive' and 'mkdir build; cd build; cmake ..; make -j8') 
$ /home/wmt/work_ppsspp/ppsspp/build/PPSSPPSDL /home/wmt/pspsdk/src/samples/gu/cube
$ /home/wmt/work_ppsspp/ppsspp/build/PPSSPPSDL `pwd`
(don't use cube.elf or EBOOT.PBP file path, use directory path instead)
```

## jpcsp  
* https://github.com/jpcsp/jpcsp  

## pcsp (? rename to pspe4all ?)    
* https://github.com/georgemoralis/pcsp  

## PPSSPP  
* https://github.com/hrydgard/ppsspp
* https://github.com/OtherCrashOverride/ppsspp-go2  
https://github.com/christianhaitian/ppsspp-go2    
* https://github.com/libretro/ppsspp  

## kene-touhou-mohofu		東方模倣風  
* https://code.google.com/archive/p/kene-touhou-mohofu/

## LUA_TH		東方PSP  
* https://psplua.xxxxxxxx.jp  

## PSP制作AVG游戏引擎-AMP vs 琳芙斯Ⅱ(ReinforceZwei)引擎		PSP引擎  

## pspsdk.rar  

## pspautotests    
* https://github.com/hrydgard/pspautotests  

## psp-homebrew-library  
* https://archive.org/details/psp-homebrew-library?page=4
* https://www.ppsspp.org/docs/getting-started/how-to-get-demos-and-homebrew/  

## PSP-Archive  
* like https://github.com/PSP-Archive/ONScripter-for-PSP
