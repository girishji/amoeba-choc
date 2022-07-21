# amoeba-choc
Single switch pcb for Kailh Choc keyboard switch (KiCad project).

If you are interested in using, here is some info:
- Use 1.2mm thickness pcb (suitable for Choc 1350 hotswap sockets)
- If you are using jlcpcb pick the option to let them panelize (5x5 will
    fit in 100x100 board ($2+shipping))
- Diodes are SOD-123 (1N4148)
- LED is SMD 6028 monochrome (you can get white ones from aliexpress). Wire
  them in a charlieplex and use IS31FL3731 LED driver (Adafruit sells a breakout
  board). 
- Some notes on LED:
    - IS31FL3731 drives (PWM) LEDs at 8k Hz. This causes audible buzz
      (annoying) from the ceramic capacitors on board of Adafruit board. To
      remove noise replace the 2 10uF capacitors with Tantalum capacitors.
      Also, you can create your own circuit for IS31FL3731 (jlcpcb stocks the
      parts) using the datasheet from Lumissil. Adafruit also has Eagle files
      on github that you can easily turn into Gerber files.
    - You can use RGB leds if you are into that. Just create two additional
      pads for soldering. You need two IS31FL3731s.
    - Do NOT use SK6812 mini-E. They are power hungry and not suitable for
      per-key LED. They are similar to sk6812 or ws2812b and they
      all have an IC inside them that does PWM. Each can draw upto 20mA. They
      draw 1mA even when turned off. You'll easily reach 500mA (or 900mA) limit
      of USB 2.0 (3.0) port. Laptop battery drains quickly. OTOH IS31FL3731
      draws 2mA (and you only need one) when LEDs are turned off and each LED get 2 or 3mA.
 - Note on soldering: You can use 'magnet wire' and eliminate the need to strip
   insulation. Get .2-.3mm single-insulation type and you can melt off the
   insulation at the tip using soldering iron and a dab of solder (there are
   some youtube videos).

  ![image](pcbv.png)

  Here are some images of keyboard built using this pcb.

  ![image](https://i.imgur.com/7HjXotx.jpg)
  ![image](https://i.imgur.com/o7rhdtJ.jpg)
  ![image](https://i.imgur.com/gi0ZL6s.jpg)
