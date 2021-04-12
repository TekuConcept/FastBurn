# FastBurn

FastBurn is an assistive utility used to flash HiSilicon cameras. (Currently only tested with the HI3516CV500 chip)

Steps:
1. Upload a fastboot image. This program-binary initializes the RAM and then waits for another binary to run.
2. Upload the uboot image. uboot already has nand/nor burning functions built in, so to keep things simple, a temporary uboot image is uploaded to RAM and executed.
3. Upload the image to burn. This is the image that will be loaded on reboot.
4. Have uboot burn the image to flash and then reboot.

It's not perfect and doesn't work 100% of the time (do to serial error or system timeouts), but it gets the job done on a linux system!
