# Fast-FIFO-test
Cf. https://www.plctalk.net/qanda/showthread.php?t=131308

Test to see if MicroLogix 1100 (ML100) can keep up while running four lines in parallel, each line with a FIFO implemented as a circular buffer, and each FIFO receiving a new value to add at a rate of just under 80Hz.

The lines are active for one continuous second at a time, from 0 to 10,000 counts of the ML1100's 10kHz Free-Running Clock (FRC), with an event generated for one line every 32 counts (3.2ms), so each line gets one event every 128 counts (12.8ms).  The first line, LINE0, accumulates 79 new values during the second (count ranges 0-31 through 9984-9999); the other three lines each accumulate 78 new values.

The image below is of the ML1100 in RUN mode, in between two active periods; the counts of values, N252:16, N253:16, N254:16, N255:16, are all consistent with the ML100 keeping up.

![](https://github.com/drbitboy/Fast-FIFO-test/raw/master/fast_fifo_running.png)
