# STM32 ST7735 LCD library.

STM32 library for displays that are based on ST7735 controller.

<img src="https://microtechnics.ru/wp-content/uploads/2021/08/podklyuchenie-st7735-k-stm32-1.jpg" width="400">

Repository includes library and project files, library is device independent and uses one SPI module and 3 GPIOs to control:

- Reset line
- CS line
- DC line

Project is built for STM32F103RE with the following settings:

- SPI1 for communication (only MOSI ans SCK needed - PB5 for MOSI signal, PB3 for SCK)
- PB7 (Reset)
- PC11 (CS)
- PB6 (DC)

Software tools:

- IDE: IAR Embedded Workbench
- STM32CubeMx
- HAL Driver

Despite the fact that HAL driver is used SPI part is written with manual registers handling because it significantly increases LCD rendering speed. A detailed description is available on my site - [STM32 ST7735 library](https://microtechnics.ru/podklyuchenie-displeya-na-baze-st7735-k-mikrokontrolleru-stm32/).
