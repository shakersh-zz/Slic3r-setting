G4
M104 S0;turn off temperature
M140 S0;turn off bed
M107;turn off fan
G1 X0 Y200; Home x,y
M84; disable motors
M300 S300 P1500
G4 S1
M300 P1500
