# rp2040-freertos-template
This is a template project for developing FreeRTOS based applications on the Raspberry Pi RP2040.

To use both cores change `configNUMBER_OF_CORES` to 2 in *FreeRTOSConfig.h*

Unmodified the project will spawn a single task to rapidly blink the LED on and off.

The *.vscode* folder configures the IDE to use **PicoProbe**.

## FreeRTOS kernel

The project uses an external copy of the FreeRTOS kernel, in the location defined by `FREERTOS_KERNEL_PATH` in the top level *CMakeLists.txt*.

### To install the kernel if you don't already have it
```sh
$ cd <some_target_directory>
$ git clone -b smp https://github.com/FreeRTOS/FreeRTOS-Kernel --recurse-submodules
```

### To update a previously downloaded kernel
```sh
$ cd <some_target_directory>/FreeRTOS-Kernel
$ git pull
```