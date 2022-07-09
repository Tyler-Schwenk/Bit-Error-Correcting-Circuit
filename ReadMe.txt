Tyler Schwenk
tylerschwenk1@yahoo.com

I designed this circuit in the spring semester of 2022 for a Computer Architecture class at San Diego State University.
The project was to impliment a 4-bit Hamming code that detects and corrects a single bit error, and detects a double bit
error in a 8-bit data transmission. This was done using LogicWorks software.

My zip file contains a 'Lab2.cct' with the full circuit that was requested,
as well as idividual cct files for the parts I designed to make the 'Lab2' circuit run, namely:

- 'ecc generator' that takes a given 8-bit user input (from two hexadecimal keyboards) and adds the 4 correct parity bits, 
    then outputing a 12-bit hamming code bus.

- '13-bit data transmission' that recieved those 12 bits and where the user can add simulated error (bit flip) to any bits.

- 'main memory' that recieves the 12 bits that may have added error, and if given:
    + No added error, outputs the same correct code on two hexadecimal displays and '0' on a third.
    + 1 flipped bit, outputs the corrected original 8 input bits on two hexadecimal displays and outputs 'C' on a third
    + 2 flipped bits, outputs the incorrect 8 error bits on two hexadecimal displays and outputs 'E' on a third

It also has my TSchwenk Library folder and the .bak counterparts to all these files.