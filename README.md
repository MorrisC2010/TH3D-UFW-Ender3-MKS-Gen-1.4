# TH3D-UFW-Ender3-MKS-Gen-1.4
TH3D Modified to work with MKS Gen V1.4 - Also has BLTouch support

Instructions

Configuration.h:

  Uncomment Line 310 to enable Ender3 MKS Gen V.14
  (optional) Uncomment appropriate line between Line 318 -324 for the type of leveling device you have (Line 324 is BLTouch)
  (Optional) Uncomment Line 487 for Bilinear Leveling (Other options have not been tested as of this commit)
  (Optional) Edit Line 497 to align with your preference
  (Optional) Uncomment Line 509 to enable Fastprobe
  Edit Line 548-549 with values from your machine. USE CALIPERS!! [Left/Front of Nozzle is (-) Right/Rear of Nozzle is (+)]
  
Configuration_backend.h

  (Optional) Set value of Line 1221 to desired Baudrate (115200 is default)
  (Required) Set value of Line 1251 to steps based on installed driver:
             A4988: #define DEFAULT_AXIS_STEPS_PER_UNIT   { 100, 100, 400, 463 } 
             DRV8825: #define DEFAULT_AXIS_STEPS_PER_UNIT   { 160, 160, 800, 200 }
  (Required) Line 1259-1262: Set value to installed drivers (A4988, DVR8825, etc)
  
Compile and Upload

Run the next codes in Pronterface or similar program

M502
M500

At this Point Level your bed manually and determine your Z Offset, Calibrate your Extruder, and Run a Test Print
