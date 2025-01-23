# RPIPicoWSNTP
Raspberry PI PicoW Exampe of the SNTP to set the Pico's RTC.

Runs under FreeRTOS and LWIP SNTP App.

Also runs simple workload to flash an LED on GPIO0.

[Video tutorial](https://youtu.be/Xv8yHjFRB08)

## Folders

+ Port: contains the library port code for the FreeRTOS and LWIP libraries. 
+ src: main source for the example

## SNTP Functions
Helper functions for SNTP are in the WifiHelper class. This also require one C function, which gets reference into  lwipopts.h

## Clone and Build
Submodule are used so clone with the command:
```
$ git clone --recurse-submodules https://github.com/jondurrant/RPIPicoWSNTP
```

To prevent leaking Wifi credentials into Github I pick these up from environment variables. These should be set in the shell or terminal before you run cmake:
+ WIFI_SSID
+ WIFI_PASSWORD

Built through cmake:
```
mkdir build
cd build
cmake ..
make
```

Binaries (elf and uf2) will be in the folder "build/src".
