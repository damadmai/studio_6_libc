# Atmel Studio 6.2 addon project for AVR projects browsing libc implementation

## Instructions

1. Download [avr-libc-source](http://distribute.atmel.no/tools/opensource/Atmel-AVR-GNU-Toolchain/3.4.5/avr-libc-1.8.0.tar.bz2)
  and put the contents of the avr-libc directory into  
  `C:\Program Files (x86)\Atmel\Atmel Toolchain\AVR8 GCC\Native\3.4.1061\avr8-gnu-toolchain\avr`.
* Clone this repository to desktop.
* Add [`libc.cproj`](./libc.cproj) to your
  [Atmel Studio 6.2 Build 1502](https://www.mikrocontroller.net/articles/Atmel_Studio) solution.
* Use Alt+G or right click and  `Goto Implementation` in editor to browse the libc source.
* Publish your project. :octocat:

## How to create it by yourself

* Create a new GCC C Static Library Project in [Atmel Studio 6.2](https://www.mikrocontroller.net/articles/Atmel_Studio)

* Add all .c .h, .S and .inc files as LINK to the project from
```
    C:\Program Files (x86)\Atmel\Atmel Toolchain\AVR8 GCC\Native\3.4.1061\avr8-gnu-toolchain\avr
    C:\Program Files (x86)\Atmel\Atmel Toolchain\AVR8 GCC\Native\3.4.1061\avr8-gnu-toolchain\avr\libc\misc
    C:\Program Files (x86)\Atmel\Atmel Toolchain\AVR8 GCC\Native\3.4.1061\avr8-gnu-toolchain\avr\libc\pmstring
    C:\Program Files (x86)\Atmel\Atmel Toolchain\AVR8 GCC\Native\3.4.1061\avr8-gnu-toolchain\avr\libc\stdio
    C:\Program Files (x86)\Atmel\Atmel Toolchain\AVR8 GCC\Native\3.4.1061\avr8-gnu-toolchain\avr\libc\stdlib
    C:\Program Files (x86)\Atmel\Atmel Toolchain\AVR8 GCC\Native\3.4.1061\avr8-gnu-toolchain\avr\libc\string
    C:\Program Files (x86)\Atmel\Atmel Toolchain\AVR8 GCC\Native\3.4.1061\avr8-gnu-toolchain\avr\common
    C:\Program Files (x86)\Atmel\Atmel Toolchain\AVR8 GCC\Native\3.4.1061\avr8-gnu-toolchain\avr\include
    C:\Program Files (x86)\Atmel\Atmel Toolchain\AVR8 GCC\Native\3.4.1061\avr8-gnu-toolchain\avr\include\compat
    C:\Program Files (x86)\Atmel\Atmel Toolchain\AVR8 GCC\Native\3.4.1061\avr8-gnu-toolchain\avr\include\util
    C:\Program Files (x86)\Atmel\Atmel Toolchain\AVR8 GCC\Native\3.4.1061\avr8-gnu-toolchain\avr\libm\fplib
```
* do the same for all files which are not of the form ioxx.h but do add:

  `"iotnx5.h" "iom8.h" "iom8a.h" "iom16u4.h" "iom32.h" "iom32a.h" "iom32u4.h" "iom88pa.h" "iom168pa.h" "iom328.h" "iom328p.h" "iomx8.h" "iotn4.h" "iotn5.h" "iotn9.h" "iotn13a.h" "iotn45.h" "iotn85.h" "iotn2313a.h"`

* Add this directory for All Configurations to the AVR/GNU C Compiler and Assembler Directories as absolute Path:

    `C:\Program Files (x86)\Atmel\Atmel Toolchain\AVR8 GCC\Native\3.4.1061\avr8-gnu-toolchain\avr\common`

## Links

German Discussion Forum Thread:
https://www.mikrocontroller.net/topic/343841

## License

[MIT](./LICENSE)
