# 555-Timer-Voltage-Multiplier-Sponsored-by-JLCPCB

Thank you JLCPCB for sponsoring this project. Please order your PCB at jlcpcb.com/RAT

This project is about using NE555 timer as an alternating current AC signal as an input to the capacitors and diodes. The capacitors and diodes produce a high voltage direct current output.

Let's get started.

![image](https://user-images.githubusercontent.com/85741357/181504530-c6731f91-be1d-407b-bd8f-90784234f0cf.png)

MT3608 DC to DC step up converter

We will need MT3608 DC to DC step up converter to convert 5V DC from a power supply such as USB charger to 15V DC to source the NE555 timer.

5V USB -> 15V DC to DC step up converter -> NE555 timer -> Capacitors and diodes

The NE555 timer has a maximum input voltage of 16V. To ensure that we do not hit the voltage threshold, we turn the MT3608 knob and measure the output voltage of the MT3608 with a multimeter and stop at 15V.

We will use a 50% duty cycle 555 timing state for our NE555 timer. The two ceramic capacitor value for the 555 timer is 10 nF each. The R1 resistor has a value of 0.5 Watt, 100k ohms. The R2 resistor has a value of 0.5 Watt, 1k ohm.

To calculate the frequency of the NE555 timer, we use

f = 1 / (0.693 * 2R2 * C)

f = 1 / (0.693 * 2 * 1000 * 10 * 10^-9)

f = 72150 Hz

The higher the frequency, the lesser the power loss at the output of the NE555 timer.

We will use 16 25V 10uF electrolytic capacitors and 16 1N4007 diode to multiply our NE555 output voltage.

The PCB circuit allows us to get the outputs of every stages of the multiplier.

At the final stage, we will get less than and around 14V * 16 = 224V.

Please handle the high voltages with care. Avoid touching any conductive leads with bare hands.

Hope you enjoy this project, and do order your PCB at jlcpcb.com/RAT
