# InkPulse: CNC XY Plotter

**InkPulse** is a custom-built, low-cost, high-speed XY-plotter designed to draw vector artwork and write text in English with different kinds of font with good accuracy. Built from scratch without expensive linear bearings. This project pushes the limits of DIY hardware optimization through low-cost 3D printing mechanism and custom firmware.
---

## Key Features

* **Low Cost Engineering:** Replaced expensive LM8UU and LM8LUU linear bearings with custom 3D-printed friction-based rod guides, lowering construction costs significantly compared to typical DIY plotters.
* **Firmware  Remapping:** Custom GRBL-Servo 0.9i firmware running at 115200 Baud Rate, remapped directly at `cpu_map_atmega328p.h` level. Y-axis pins (Step: 4, Dir: 7) were swapped with Z-axis pins as here was a hardware issue in the arduino I used in this priject, (Step: 3, Dir: 6) to drive the pen lift via standard Z+ slot G-code commands (`M3 S13`/`M5 S40`).
* **High Speed & Acceleration:** Powered by a 19V 3.15A DC power supply and GT2 belt-drive system, tuned to achieve up to 8000 mm/min maximum feed rate and **500 mm/sec²** acceleration.

## Working Principle
There are 2 stepper motors that controls respectively X and Y axis. So the pen can go to anywhere in the grid. The servo  motor controls the z axis mechanism or pen lifting mechanism. The whole thing's brain is Arduino Uno. The CNC shield v3 sits on the top of Arduino. and 2 A4988 Stepper Drivers sit on the CNC shield completing the control unit. The servo is connected by 3 wires that is connected by a custom made bridge so that the wire can go wherever the pen moves. And a 12v DC motor connected with 19v with a resistor in series that cools the control unit where plenty heat is produced by A4988 Stepper Drivers.

## Softwares
The Inkpulse uses several software to operate. Firstly comes the Gcode part. The Gcode is written by Inkscape software with 4xiDraw Control and KM LAser extension. Inkscape creates a trace bitmap and it converts it into gcode. Then LaserGRBL sends those Gcode to the Inkpulse and it can write or draw smoothly.


---

## Hardware & Components List

| Component | Description |
| :--- | :--- |
| **Controller** | Arduino Uno R3 |
| **Shield** | CNC Shield V3 |
| **Drivers** | A4988 Stepper Drivers (1/16 microstepping) |
|**Motors** | Nema 17 45Ncm stepper motor|
| **Power Supply** | 19V 3.15A DC Adapter |
| **Pen Lift** | SG90 / MG90S Micro Servo Motor |
| **Drive System** | GT2 Belts & 20-Tooth Pulleys |
| **Structure** | Custom 3D Printed Rod Guides + Smooth Steel Rods |
| **Power Filter**| 1000uF Electrolytic Capacitor |
|**Others**| Cooling fan, holding parts(screw, zip tie) |

---

## 3D Objects
### In Fusion 360 Application
<img width="1215" height="686" alt="image" src="https://github.com/user-attachments/assets/817f16e0-917f-48cc-b862-1a83d21bb610" />
<img width="763" height="605" alt="image" src="https://github.com/user-attachments/assets/77085ad3-a0cf-4e21-85a8-d7b83b7c9db7" />
<img width="1093" height="678" alt="image" src="https://github.com/user-attachments/assets/f9ecba63-2c46-490f-a1f2-3be7fd6f5603" />
<img width="868" height="551" alt="image" src="https://github.com/user-attachments/assets/7c351e64-69fa-4562-bef5-5b90a5da913b" />
<img width="780" height="717" alt="image" src="https://github.com/user-attachments/assets/247b6640-9cf2-4402-96e1-60417e5f86dc" />
<img width="1093" height="794" alt="image" src="https://github.com/user-attachments/assets/2e98e916-141b-47ad-8f6d-50c296d60b76" />
<img width="978" height="737" alt="image" src="https://github.com/user-attachments/assets/20e260d1-a3e0-460f-bca1-1750db618607" />


<img width="1417" height="910" alt="image" src="https://github.com/user-attachments/assets/cb263346-3972-4396-9f15-0348ea5fc7d7" />



## 📷 Photos & Video Demonstration

### Project Build & Working Demo
<img width="1600" height="1200" alt="image" src="https://github.com/user-attachments/assets/7ee0811f-c7fd-4dc2-b9c7-cf2565ca1892" />
<img width="2048" height="1536" alt="image" src="https://github.com/user-attachments/assets/a697499c-f397-4926-a9d9-f17e65e18785" />
<img width="960" height="1280" alt="image" src="https://github.com/user-attachments/assets/41de2647-f42b-40fd-8c54-d49aa975f42c" />


**Watch Its Working Video** [Click here to view the plotter in action](WhatsApp%20Video%202026-10-04%20at%2010.53.54%20PM_squished.mp4)

## Repository Structure
* `/3D objects` All the 3d printable .3mf file


---

