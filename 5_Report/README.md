# Introduction

The system is used to warm the seates of automobiles when used in cold freezing winters.
Heated seats can make cars much more comfortable in the winter, or for those who often get cold even in the summer. The heater in most vehicles work well, but the car's seat warmer is close to your body allowing you to warm up faster.
### Input and connections
- Seat switch (D0)
- Heat switch (D1)
- Heat adjust potentiometer (C0)
### Output
- Heater LED (B0)
- 4 heat-level indicator (B2 & B3)
- Oscilloscope (B1)
Pins B2 and B3 are connected to a 4 heat-level indicator through a logic circuit to show the increasing heat levels.


## Circuit
 


![1](https://user-images.githubusercontent.com/102032303/164615045-7e1d4793-18f1-4712-9c8b-8f82e9329e6e.png)

# Requirements
## Introduction
Automobiles used in the cold regions must have seat heater along with the air-conditioning system. This ensures more comfort to the driver by adjusting the environment temperature close to nominal body temperature.

### Advantages
- Comfortable driving experience.
- Faster heating of seats and reduced dependancy of AC heater.

### Disadvantages
- Should be adjusted manually and cause distraction.

## SWOT Analysis
### Strength
- Ability to change temperature setting through the code
- Manual control of temperature adjustment
- Manual switching operation
- Limited temperature range

### Weakness
- No feedback loop to check temperature
- Fails to detect malfunction

### Opportunity
- To adapt with the AC environment settings
- To detect error if malfunctions

### Threat
- Excessive heating can damage the seat

## 4 W's and 1 H

### Who
- The driver and passengers.
### What
- Heated seats for more comfort.
### When
- Very effective during cold winters.
### Where
- In the seats of the automobile.
### How
- Heating system within the seat.

## High Level Requirements



|ID|	Description	|Status (Implemented/Future)|
| :-------- | :------- | :------------------------- |
|HR01|	Supply PWM signals based on the required temperature	|Implemented|
|HR02|	Should only be activated when the driver is seated	|Implemented|
|HR03|	Should be able to turn OFF manually	|Implemented|


## Low Level Requirement
|ID|Description	|Status (Implemented/Future)|
| :-------- | :------- | :------------------------- |
|LR01 |	Specify the duty cycles based on the temperature|	Implemented|
|LR02 |	Reliability of the switch connected to the seat	|Implemented|
|LR03 |	Switch to manually turn ON and turn OFF the seat heater|	Implemented|

# Design

## Flow Chart


![3](https://user-images.githubusercontent.com/102032303/164625741-869d2f8e-e67c-4926-9f74-96d898ef7fc9.png)


# Simulations
## Heating System is OFF
- System OFF: Power supply is turned OFF
- Driver absent Heater OFF: SEAT SWITCH OFF and HEAT SWITCH OFF

| System OFF|	Driver absent Heater OFF|
| :-------- | :------- | 
|![Soff](https://user-images.githubusercontent.com/102032303/164645802-a72d7f71-6341-4d6c-9b3d-9ef5e64d22f4.png)  | ![doff](https://user-images.githubusercontent.com/102032303/164645852-d7ee7e58-74a1-4916-84aa-dbffd1b7c976.png) |



- Driver absent Heater ON: SEAT SWITCH OFF and HEAT SWITCH ON
- Driver present Heater OFF: SEAT SWITCH ON and HEAT SWITCH OFF


|Driver absent Heater ON|	Driver Present Heater OFF|
| :-------- | :------- | 
|![dahon](https://user-images.githubusercontent.com/102032303/164646372-a706f55e-fe20-4ef7-b090-bcf397240cce.png)| ![dphoff](https://user-images.githubusercontent.com/102032303/164646429-3e51f1c8-0c2f-4aac-89dc-e98ba9b5608b.png) |


## Heating System is ON with four levels
- Heater ON Level 1:
   -  SEAT SWITCH ON, HEAT SWITCH ON, HEATER LED ON
   - HEAT ADJUST POT 20%, 4 HEAT-LEVEL LED INDICATOR in level 1
   - Oscilloscope showing 20% duty cycle
- Heater ON Level 2:
   - SEAT SWITCH ON, HEAT SWITCH ON, HEATER LED ON
   - HEAT ADJUST POT 40%, 4 HEAT-LEVEL LED INDICATOR in level 2
   - Oscilloscope showing 40% duty cycle

|HeaterOn Level 1|	HeaterOn Level 2|
| :-------- | :------- | 
| ![honl1](https://user-images.githubusercontent.com/102032303/164646662-0830ab45-ef63-42ea-b70b-0d222cbba77a.png)| ![honl2](https://user-images.githubusercontent.com/102032303/164646746-a6a3f606-3764-41c6-97a3-172876b87211.png)|


- Heater ON Level 3:
   - SEAT SWITCH ON, HEAT SWITCH ON, HEATER LED ON
   - HEAT ADJUST POT 70%, 4 HEAT-LEVEL LED INDICATOR in level 3
   - Oscilloscope showing 70% duty cycle
- Heater ON Level 4:
   - SEAT SWITCH ON, HEAT SWITCH ON, HEATER LED ON
   - HEAT ADJUST POT 95%, 4 HEAT-LEVEL LED INDICATOR in level 4
   - Oscilloscope showing 95% duty cycle
   
|HeaterOn Level 3	|HeaterOn Level 4|
| :-------- | :------- | 
|![honl3](https://user-images.githubusercontent.com/102032303/164647180-014cd3b6-b39c-4a39-acad-2e60a1f29d88.png) |![honl4](https://user-images.githubusercontent.com/102032303/164647214-2d8963f4-b79f-4a90-9c6a-9b3d99624a4c.png) |
