
Youyue-858D-plus
================

Custom firmware for the Youyue 858D+ (ATmega168/ATmega328)

There is a 'user manual' of sorts in the 'Docs' folder.

Some videos showing the progress from 'stock firmware' with massive temperature overshoot
towards almost no overshoot at all.

https://www.youtube.com/playlist?list=PLONcxJMOrdyeYuEgM6qhCllZelN6gPjrT


Please note:

Although this device looks very much like ones sold by 'Atten' and others, the innards
are not necessarily the same. The heater / wand are probably the same, but I know that
e.g. the 'Atten 858D' uses a different mainboard with a different brand micro controller.

Naturally, this firmware will only work 'as is' for the exact mcu / mainboard combination I have.
Please see the 'Docs' folder for schematic and PCB photos.

MCU-Adapter [repository](//github.com/madworm/Youyue-858D-plus-MCU-adapter) (optional).

Compiling/Development
=====================
There are currently three options available, choose your preferred environemt:
* Use the [https://www.arduino.cc/en/Main/Software](Arduino IDE), make sure you do ISP Upload and _don't_ use the arduino bootloader.
* Use [http://www.atmel.com/microsite/atmel_studio6/](Atmel Studio 6) together with the [http://www.visualmicro.com/page/Arduino-for-Atmel-Studio.aspx](VisualMicro Plugin) for Arduino support, make sure you do ISP Upload and _don't_ use the arduino bootloader.
* "raw" text editing and Makefiles, to do so run `git submodule update --init` and afterwards `make ispload`. You probably need to adjust `ISP_PROG` and `AVRDUDE_ARD_PROGRAMMER` in the makefile.

The supplied `release.sh` only works together with the Makefile method.

---

Safety information / disclaimer:
================================

Making any modifications to this device may cause you irreversible physical harm or worse.
You do this at your own risk. 

There is a significant risk of lethal electrical shock, so if you still insist of doing so, make sure to
ALWAYS UNPLUG THE MAINS CABLE before dismantling the device. Check repeatedly.

If you have an isolation transformer - do use it.

