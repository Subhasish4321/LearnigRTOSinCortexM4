Each real time kernel port consists of three files that contain the core kernel
components and are common to every port, and one or more files that are 
specific to a particular microcontroller and or compiler.

+ The FreeRTOS/Source directory contains the three files that are common to 
every port - list.c, queue.c and tasks.c.  The kernel is contained within these 
three files.  croutine.c implements the optional co-routine functionality - which
is normally only used on very memory limited systems.

+ The FreeRTOS/Source/Portable directory contains the files that are specific to 
a particular microcontroller and or compiler.

+ The FreeRTOS/Source/include directory contains the real time kernel header 
files.

See the readme file in the FreeRTOS/Source/Portable directory for more 
information.


*****Personal Note**************************************************************************
For segger to read the event trace stored in RTT buffer the buffer address can be read from
the Expression tab by:
1. Find the expression: _SEGGER_RTT 
2.It contains the buffer address under aUp[1] in the pointer called pBuffer
3.To take the event dump,use the memory browser window,give the address and the size of memory to read.
4.export the data with extension .SVdat and select raw memory type when exporting. Checking