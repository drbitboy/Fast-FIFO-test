# Fast-FIFO-test
Cf. https://www.plctalk.net/qanda/showthread.php?t=131308

MicroLogix 1100 running four lines in parallel, each line with a FIFO implemented as a circular buffer, and each FIFO receiving a new value to add at a rate of just under 80Hz (~3.2ms per event for all four).
