# USBX CDC Test Project for STM32U585

This is an initial project demonstrating USB CDC (Communication Device Class) functionality for the **WeAct Studio Black Pill STM32U585** board using Azure RTOS USBX middleware.

## Key Features

- ✅ USB CDC implementation using USBX middleware
- ✅ Compatible with **STM32CubeIDE** (unlike the official WeAct Studio example)
- ✅ Also works with **MDK-ARM/Keil**
- ✅ Based on STM32U5 HAL drivers
- ✅ Configured for STM32U585CIUx microcontroller

## What Makes This Special

The official WeAct Studio example projects for the STM32U585 Black Pill typically only support MDK-ARM (Keil). This project provides a working configuration for both:

- **STM32CubeIDE** - Free, Eclipse-based IDE from ST
- **MDK-ARM** - Keil's professional ARM development environment

This makes the project more accessible to developers who prefer or require STM32CubeIDE for their development workflow.

## Hardware

- **Board:** WeAct Studio STM32U585 Black Pill
- **MCU:** STM32U585CIUx
- **USB:** USB OTG Full Speed

## Project Structure

```text
├── Core/                    # Application core files (main.c, initialization)
├── Drivers/                 # STM32U5 HAL and CMSIS drivers
├── Middlewares/             # USBX middleware stack
├── USBX/                    # USB application and target files
├── MDK-ARM/                 # Keil MDK-ARM project files
├── STM32CubeIDE/           # STM32CubeIDE project files
└── usbx_test.ioc           # STM32CubeMX configuration file
```

## Getting Started

### Prerequisites

Choose one of the following IDEs:

- **STM32CubeIDE** (recommended, free) - [Download here](https://www.st.com/en/development-tools/stm32cubeide.html)
- **MDK-ARM/Keil** - Commercial IDE

### Building with STM32CubeIDE

1. Open STM32CubeIDE
2. Import the project: `File` → `Open Projects from File System`
3. Select the `STM32CubeIDE` folder
4. Build the project
5. Flash to your STM32U585 Black Pill board

### Building with MDK-ARM

1. Open Keil µVision
2. Open the project file: `MDK-ARM/usbx_test.uvprojx`
3. Build the project
4. Flash to your board

## Configuration

The project is pre-configured with STM32CubeMX (`.ioc` file). You can modify the configuration by:

1. Opening `usbx_test.ioc` in STM32CubeMX
2. Making your changes
3. Regenerating the code

## USB CDC Functionality

This project implements a USB CDC device, which appears as a virtual COM port on your PC. You can:

- Communicate with the device using any serial terminal
- Send and receive data over USB
- Use standard COM port drivers (no custom drivers needed)

## License

Please refer to the individual license files in the `Drivers` and `Middlewares` directories for ST's HAL drivers and USBX middleware.

## Resources

- [WeAct Studio STM32U585 GitHub](https://github.com/WeActStudio/WeActStudio.STM32U585CoreBoard)
- [STM32U5 Documentation](https://www.st.com/en/microcontrollers-microprocessors/stm32u5-series.html)
- [Azure RTOS USBX Documentation](https://learn.microsoft.com/en-us/azure/rtos/usbx/)

## Contributing

Feel free to submit issues or pull requests if you find bugs or have improvements to suggest.
