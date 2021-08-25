# orbisdev
Main PS4 Repo for building the whole `Orbis Development` environment in your local machine.

![CI](https://github.com/orbisdev/orbisdev/workflows/CI/badge.svg)
![CI-Docker](https://github.com/orbisdev/orbisdev/workflows/CI-Docker/badge.svg)

This program will automatically build and install the whole a compiler and other tools used in the creation of homebrew software for the Sony PlayStation® 4 videogame system.

## What these scripts do

These scripts download (`git clone`) and install: 
- [orbisdev-toolchain](https://github.com/orbisdev/orbisdev-toolchain "orbisdev-toolchain") 
- [orbisdev-sdkvanilla](https://github.com/orbisdev/orbisdev-sdkvanilla "orbisdev-sdkvanilla") 
- [orbisdev-liborbis](https://github.com/orbisdev/orbisdev-liborbis "orbisdev-liborbis") 
- [orbisdev-orbisGl](https://github.com/orbisdev/orbisdev-orbisGl "orbisdev-orbisGl") 
- [orbisdev-orbisGl2](https://github.com/orbisdev/orbisdev-orbisGl2 "orbisdev-orbisGl2")

## Requirements

1. Install clang, make, patch, git, texinfo wget, bison, flex and m4 if you don't have those.

2. Add this to your login script (example: ~/.bash_profile)  
```
export ORBISDEV=/usr/local/orbisdev
export PATH=$ORBISDEV/bin:$PATH
```

3. Run build-all.sh  
```
./build-all.sh
```

## Docker generation
This repo also uses CI/CD to create a docker image called `orbisdev/orbisdev:latest`per change. This is quite useful if you're a developer that want to create/port an application to the PS4. So, you just can go there and compile your project using this docker image.

## Extra steps
If you want, you *JUST* can install the extra dependencies as `orbisdev-orbisGl and orbisdev-orbisGl2`, to achieve this just execute

```
./build-extra.sh
```

## Thanks
