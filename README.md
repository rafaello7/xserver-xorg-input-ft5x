## Xorg multitouch touchscreen driver for ft5x chip.

Note that the driver may not work correctly with some tablets having ft5x chip
on board. This is because the chip real driver is in Linux kernel and the
kernel driver communicates with userland tools (like this driver) via special
file located in /dev/input directory. The communication protocol does not
depend on chip but on the kernel driver implementation. Implementations from
different vendors may differ in the reported device name and in some
communication details.

On the other hand, it may turn out that driver works properly with
tablets having quite different chip (to test this, some changes in Xorg
configuration file are needed).

Note also that binary packages may not work with some Xorg versions (or may
stop to work after Xorg server upgrade). This may occur because Xorg server
checks ABI version which the driver was compiled with and does not use the
driver when the version does not match. To fix the problem, the driver
re-compilation is needed.


This driver was tested with Ainol Novo 7 Aurora (having Allwinner A10 chip) and
with Cube U30GT-H, which has Rockchip RK3066 chip on board.


## Mouse handling

1. Tap with one finger - click on this position
2. Press and drag finger - move cursor, touchpad-like
3. Press on the right, then tap on the left - click left mouse button
4. Press on the left, theh tap on the right - click right mouse button
5. Press with one finger and drag with second one - scroll (like
        mouse wheel -- both hotizontal and vertical scrolling is emulated)
6. Press with one finger, then press with second, then drag with first
    one - drag


