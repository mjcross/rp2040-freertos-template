# rp2040-freertos-template
This is a template project for developing FreeRTOS based applications on Raspberry Pi RP2040 based boards. This template uses the "official" RP2040 port from the Raspberry Pi Foundation. My previous repo used the generic Cortex M0 port so this one corrects that. Previous Repo retained as tutorials rely on it. 

Unmodified, this project will spawn a single task to rapidly blink the LED on and off.

## Build environment
As downloaded the project includes a freestanding copy of the FreeRTOS kernel. That's good for a quick start but probably isn't what you want for a production environment. 

To use a shared copy of the kernel, change `FREERTOS_KERNEL_PATH` in the top level *CMakeLists.txt*.

I've added a *.vscode* folder to configure the project to use **PicoProbe**.