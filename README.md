# STM32F103-UART_With_DMA
This C code is a main program file targeting a microcontroller, likely an STM32 microcontroller, using USART communication and DMA (Direct Memory Access) for data transfer. Let's go through the key components of the code:

Includes:
The code includes various header files representing different libraries used in the project. These headers provide access to functions and constants required for the peripherals and libraries used in the application.
![uart_hardware](https://github.com/ivias2000/STM32F103-UART_With_DMA/assets/125237611/c2949cfe-6004-4bc1-a844-a32012a4ae2c)

Global Variables:

data: An array of 8 bytes, presumably used to store received data.
i: An integer variable, currently commented out, and not used in the code.
b: An array of integers initialized with {2, 9}.
Enum Definition:
A custom enumeration type sta is defined with two possible values: ok and not_okey (a typo for "not_okay"). Later, two variables l and j of this type are declared.

Main Function:
The main function is the entry point of the program. It initializes the microcontroller's peripherals, sets up USART communication using DMA, and enters an infinite loop.

System Clock Configuration:
The SystemClock_Config function configures the system clock for the microcontroller.

Infinite Loop:
Within the infinite loop, the code performs the following tasks repeatedly:

Sets l to ok and checks if l is equal to ok. If true, it sets j to not_okey.
Writes a logic high to GPIO pin PA10 (presumably to control an external device).
Transmits the contents of the b array (2 bytes) through the USART1 interface.
Receives 8 bytes of data from the USART1 interface using DMA and stores it in the data array.![Screenshot 2023-07-18 112112](https://github.com/ivias2000/STM32F103-UART_With_DMA/assets/125237611/5e35aa16-be55-490e-8bc5-c4eee2ea5b5c)

Please note that some parts of the code are commented out (//), and there are unused variables (i) and unexpected typos (not_okey). It's a good practice to remove any commented-out code and unused variables before pushing your code to GitHub.

To use this code on GitHub, follow the steps mentioned earlier to create a new repository and upload this C code as the main program file. Additionally, you can include a README.md file in your repository to provide more information about the project and how to use the code.
