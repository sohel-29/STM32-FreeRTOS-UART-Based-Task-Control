# STM32-FreeRTOS-UART-Based-Task-Control
This project demonstrates task management in FreeRTOS using UART commands on the STM32F446RE microcontroller.
Overview

The application consists of three FreeRTOS tasks:

Task 1: Controls LED1 blinking on PA5.
Task 2: Controls LED2 blinking on PA6.
Task 3: Handles UART communication and task switching.

At startup:

Task 1 is active.
Task 2 is suspended.

The UART task listens for commands from a serial terminal and dynamically controls task execution.

UART Commands

Command	Action
'1'	Suspend Task 1 and Resume Task 2
'2'	Suspend Task 2 and Resume Task 1

Hardware Used

STM32F446RE
FreeRTOS (CMSIS-RTOS V2)
UART2 (115200 Baud)
Two LEDs
STM32CubeIDE
Concepts Demonstrated
FreeRTOS Task Creation
Task Scheduling
Task Suspend/Resume
UART Communication
GPIO Control
Real-Time Embedded Systems

Project Flow
System initializes GPIO and UART peripherals.
FreeRTOS scheduler starts.
Task 1 begins blinking LED1.
UART task waits for user commands.
Receiving '1' activates LED2 task and suspends LED1 task.
Receiving '2' activates LED1 task and suspends LED2 task.

Tools

STM32CubeIDE
STM32 HAL Drivers
FreeRTOS
Cool Term

Author

Sohel Mohammed
Embedded Systems | STM32 | FreeRTOS | Embedded C
