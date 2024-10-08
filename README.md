# John Deere Sprayer Control System

Main project in collaboration with *John Deere* for the undergrad course “**Analysis of Control Systems**”, which delves mainly into *Classic and Modern Control*.

<p align="center">
  <img src="https://github.com/user-attachments/assets/d9fcd6d7-fb5b-44bf-84cf-5ca00228ec28" alt = "NUCLEO-F103RB" width="300" height="300"/>
</p>

The John Deere Sprayer Control System is a computerized irrigation management solution designed to stabilize the operation of a 3D-printed sprayer model. Utilizing the NUCLEO-F103RB development board equipped with the STM32F103RB MCU, this project provides control over a DC motor to which the sprayer model is attached.

## PID Controller using Analog Electronics

As a first approach before computerization, a PID controller was implemented using analog electronics. The physical configuration consists of a 12V DC motor placed on a base that allows aligning its rotation axis in front of an AS5600 magnetic encoder, in order to know the position of the shaft and close the loop.

In the initial stage, the circuit receives the reference signal (desired value, adjusted with a potentiometer) and the signal coming from the encoder (feedback, output of the system). Both are subtracted to obtain the error signal, which is then fed to the PID. The proportional gain is intended to correct the current error, the integral gain to eliminate the error accumulated over time, and the derivative gain to anticipate future errors and smooth the system response.
