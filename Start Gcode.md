M83 ;extruder relative mode
M140 S[first_layer_bed_temperature] ; set bed temp
M104 S[first_layer_temperature] ; set extruder temp
M190 S[first_layer_bed_temperature] ; wait for bed temp
M109 S[first_layer_temperature] ; wait for extruder temp
;retract filament to prevent oozing
G92 E0 ; reset extruder location
G1 F500 E-8 ; retract by -8
G92 E0 ; reset again
G28 ; home all without mesh bed level
G29 P0; wipe old mesh
G29 P1; mesh bed leveling
G29 P3 T;mesh bed leveling
G29 A; Activate Mesh bed leveling
M300 S300 P1500
G4 S1
M300 P1500
G1 X0 Y-1 F4000.0; go outside print area

