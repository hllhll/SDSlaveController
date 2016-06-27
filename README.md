# SDSlaveController
Trying to implement SD (Secure Digital / MMC / TransFlash) SLAVE device for sd card emulation.

My goal is to be able to connect a physical sd card to any sd card reader and `serve` it virtually;
I would like to be able to program the virtual card and manipulate as much as possible in the protocol and the actual information that goes through to the reader that is not possible currently on native sd cards.

Since the sd card protocol starts at speeds of ~500kbps it is a bit too fast (if i'm wrong please tell me) to bit-bang on most microcontrollers. So, the idea here is to implement, first, an IP-Core that would offload the basic parts of the protocol. This would be written in HDL, and *hopefully* be converted to a Wishbone (bus) periphial to be used with ZPUino
