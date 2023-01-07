# Bit Error Correcting Circuit Design in LogicWorks

## Goal
To create a circuit that is able to detect and correct errors in 8 bits of transmitted data. To do this I implimented a 5-bit Hamming code that is able to detect and correct a single bit error, and detect a double bit error but not correct it. This was done using LogicWorks software.

## Overview
The circuit allows the user to input 2 hexadecimal numbers which are converted to 8 bits of binary. In the ECC generator the 5 appropriate parity bits are created using XOR gates which will be sent out as our final simulated output from the user. These will then go through a 13 bit transmission. In the real world this could be a variety of transmission methods such as a wire or broadcast, any of which could have noise. In my case I have 13 switches that are XOR'ed into the bits of the data transmission bus to simulate my own error in transmission. These bits (potentially containing error) are fed into the main memory which processes them and displays 3 hexacecimal digits to the output as such:
  + No added error, outputs the same correct code on two hexadecimal displays and '0' on a third.
  + 1 bit in error, outputs the corrected original 8 input bits on two hexadecimal displays and outputs 'C' on a third
  + 2 bits in error, outputs the 8 bits with error on two hexadecimal displays and outputs 'E' on a third
![](/overview.jpg)

## Inside each part

### ECC Generator
- Takes a given 8-bit user input (from two hexadecimal keyboards) and adds the 5 correct parity bits, then outputs a 13-bit hamming code bus.
![](/ECCgenerator.jpg)

### 13-bit Data Transmission
-  Where the user can add simulated error (bit flip) to any bits.
![](/DataTransmission.jpg)

### Main Memory
- Recieves the 13 bits and finds any error, fixes it if possible, and reports the final output data and error code.
![](/MainMemory.jpg)
