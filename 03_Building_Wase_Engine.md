To build Wase Engine you will need to install the following tools:  
- C++17 or higher  
- CMake  
- SDL2  
- SDL2 Image  
- SDL2 Mixer  
- SDL2 TTF  
  
**CMake**
  
```  
mkdir build  
cd build  
cmake ..  
cmake build .  
```

**MinGW**
```
mkdir build
cd build
cmake -G "MinGW Makefiles" ..
make
```

To add testing to your build you can add the additional commandline argument `-D enable_test=1` and run `ctest` in the test folder.