# amoeba-choc
Single switch pcb for Kailh Choc keyboard switch (KICad project).

If you are interested in using, here is some info:
- Use 1.2mm thickness pcb
- If you are using jlcpcb pick the option to let them panelize (5x5 will
    fit in 100x100 board ($2+shipping)
- Use Choc 1350 hotswap sockets
- Diodes are SMD-123 (1N4148)
- LED is SMD 6028 monochrome (you can get white ones from aliexpress). Wire
  them in a charlieplex and use IS31FL3731 LED driver (Adafruit has a breakout
  board ready to use). 
- Some notes on LED:
    - IS31FL3731 drives (PWM) LEDs at 8k Hz. This causes audible buzz
      (annoying) from the ceramic capacitors on board of Adafruit board. To
      remove noise replace capacitors over 1uF with Tantalum capacitors.
      Also, you can create your own circuit for IS31FL3731 (jlcpcb has them) 
      using the datasheet.
    - You can use RBG leds if you are into that. Just create two additional
      pads for soldering. You need two IS31FL3731s.

  ![image](pcbv.png)
