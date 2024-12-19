# Just a test program

Screenshot from oscilloscope showing 223 KHz output from DAC (purple), which run in interrupt routine triggered by the timer, which also outputs its signal as a 111.5 kHz square wave (yellow):

![Screenshot 2024-12-19 014416](https://github.com/user-attachments/assets/c9c9310f-8a64-4960-8ec4-2399e5e7b2e9)

Uses about 5 mA when use internal 20 MHz clock.  If slow down to 333.333 kHz clock, then when outputting at much lower sampling rate of 1.24 kHz, then consumption drops to 1 mA:

![Screenshot 2024-12-19 020825](https://github.com/user-attachments/assets/c32c6ec5-7e58-4e52-8b6a-f364377e06f3)

Should try to find a sweet spot for low power consumptino and reasonable output rate. Note the slope of the transition takes a little over 1 us, regardless of the clock speed.
