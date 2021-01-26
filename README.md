# SDL2-Demo
This is setup guide for SDL2 project

## Linux
Prequisites: ```SDL-2```, ```SDL-2-Image```

To setup the nesscessary packages:

```bash

sudo apt-get update &&\
sudo apt-get install -y libsdl2-image-dev\ 
libsdl2-dev --fix-missing

```
After install the developer versions of SDL2 and SDL2_image:

```
cd SDL2-Demo
mkdir build
cd build
cmake ..
make
./MyGame
```

## Windows x64

Assuming CodeBlock 20.03 is installed (with MinGW64)

### Step 1: Download SDL-2 Library 
- Download the SDL-2 from this link [SDL](https://libsdl.org/release/SDL2-devel-2.0.14-mingw.tar.gz)
- Extract the file, for example, to ```C:\Users\ADMIN\Downloads\SDL2-devel-2.0.14-mingw\SDL2-2.0.14```
-- Copy all file from ```C:\Users\ADMIN\Downloads\SDL2-devel-2.0.14-mingw\SDL2-2.0.14\x86_64-w64-mingw32\bin``` to ```C:\Windows\system32``` and ```C:\Windows\sysWoW64```


### Step 2: Create new SDL2.0 project 
- From CB Select ```file->new->project...->SDL2.0```

- Enter project name and choose the path to SDL2 library eg. ```C:\Users\ADMIN\Downloads\SDL2-devel-2.0.14-mingw\SDL2-2.0.14\x86_64-w64-mingw32\```
- Choose GNU/GPL compiler (this is selected by default, if not, please reinstall CB with MinGW64)

### Step 3: Add SDL-2 linker to project  
- From project name (with colored windows icon), right click to select ```build options```
- Click ```search directory```
- From ```Compiler option``` choose ```Add``` , paste the path ```<path-to-sdl-2>\SDL2-2.0.14\x86_64-w64-mingw32\include\SDL2``` and confirm
- From ```Linker option``` choose ```Add``` , paste the path ```<path-to-sdl-2>\SDL2-2.0.14\x86_64-w64-mingw32\lib``` and confirm
### Step 4: build and run example.
- Build and Run the project
