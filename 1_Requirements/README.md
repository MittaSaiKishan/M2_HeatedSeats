
# Requirements
## Introduction
Automobiles used in the cold regions must have seat heater along with the air-conditioning system. This ensures more comfort to the driver by adjusting the environment temperature close to nominal body temperature.

### Advantages

- Faster heating of seats and reduced dependancy of AC heater.
- Comfortable driving experience.

### Disadvantages
- Should be adjusted manually and cause distraction.

## SWOT Analysis
### Strength

- Manual control of temperature adjustment
- Ability to change temperature setting through the code
- Limited temperature range

### Weakness
- Fails to detect malfunction
- No feedback loop to check temperature


### Opportunity
- To detect error if malfunctions
- To adapt with the AC environment settings


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



