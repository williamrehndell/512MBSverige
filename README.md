# 512MBSverige
**Kolla så att använder rätt profil för rätt filament! **


Dessa profiler är för Prusa **MK3S+/MK3** i Slicern Cura. 
**Följande start G-Koder skall användas för bästa resultat. **

Klistra in dessa i Settings > Printer > Manage Printer(s) > Original Prusa I3 MK3S/MK3 > Machine Settings > Start G-Code > CRTL + A > DELETE > Sen kopiera in dem som är under 

G21 ; set units to millimeters
G90 ; use absolute positioning
M82 ; absolute extrusion mode
M104 S150
M190 S{material_bed_temperature_layer_0} ; wait for bed temp
M0 S300
G28 W ; home all without mesh bed level
G80 ; mesh bed leveling
M104 S{material_print_temperature_layer_0} ; set extruder temp
M109 S{material_print_temperature_layer_0} ; wait for extruder temp
G92 E0.0 ; reset extruder distance position
G1 Y-3.0 F1000.0 ; go outside print area
G1 X60.0 E9.0 F1000.0 ; intro line
G1 X100.0 E21.5 F1000.0 ; intro line
G92 E0.0 ; reset extruder distance position


**Hur du lägger till nya profiler **
Settings > Printer > Manage Printer(s) > Profiles > Import > Välj sedan profilen du har laddat ner. 

