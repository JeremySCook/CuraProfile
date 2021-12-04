# CuraProfile
Start/end code for  Moniprice Maker Ultimate V2


;(**** start.gcode for Ultimate2 (150S)****)  
M104 S150
M84 S0 ; disable stepper idle timeout 11/29/2020 JC
G28 ; Home extruder
G92 X200 Y150 Z170.2 ;set start adedd .2 for bed adhesion
G29
G1 Z15 F100
M107 ; Turn off fan
G90 ; Absolute positioning
M82 ; Extruder in absolute mode
M109 S205 ;set extruder temperature
G92 E0 ; Reset extruder position
G1 X140 Y7 Z0.27 F4000
G1 X40 Y7 Z0.27 E23 F1000
G92 E0


;(**** end.gcode for Ultimate2 (150S)****)  
M104 S0  
M140 S0  
;Retract the filament  
G92 E1  
G1 E-1 F300  
G28  
M84  
