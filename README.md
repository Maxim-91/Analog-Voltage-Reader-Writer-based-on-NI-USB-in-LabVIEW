# NI-USB-600x Analog Voltage Reader/Writer

**NI-USB-600x Analog Voltage Reader/Writer** is a LabVIEW program designed for interfacing with the NI-USB-600x series device to generate and read analog voltages. This program uses the NI-DAQmx driver to control analog input/output operations and allows the user to write a voltage to a specific channel, then read the resulting signal.

## Features:
- **Analog Output (AO)**: Generates and writes an analog voltage within a specified range (0 to 5V) to a selected output channel.
- **Analog Input (AI)**: Reads an analog voltage from an input channel and displays the result.
- **Data Logging**: Records the output and input voltages for further analysis.
  
## How It Works:
1. **Analog Output Section**:
   - The program configures the analog output channel (`Dev1/ao0`) to write voltages between 0 and 5 volts.
   - The generated voltage is applied to the output, and a logging function captures the output voltage.

2. **Analog Input Section**:
   - The program reads analog voltages from the input channel (`Dev1/ai0`).
   - It processes and displays the measured values from the input signal, which can also be logged.

3. **Loop**:
   - The entire process of writing and reading voltages is repeated in a loop, allowing continuous monitoring and control of the voltages.

## Requirements:
- LabVIEW (with NI-DAQmx drivers installed)
- NI-USB-600x device (e.g., USB-6008, USB-6009)
- Proper connection to analog input/output terminals

## Usage:
1. **Configure the Input/Output Channels**: 
   - By default, the program uses `Dev1/ai0` for analog input and `Dev1/ao0` for analog output. Ensure that these channels are properly connected to your hardware.
   
2. **Run the Program**:
   - After starting the program, it will continuously write a voltage to the output and simultaneously read the voltage from the input.
   
3. **Logging**:
   - Both the output and input values are logged and displayed in real-time. This data can be used for later analysis.

4. **Stop Condition**:
   - The program includes a stop button that allows for safe termination of the continuous read/write loop.

## Example:
- The program generates a voltage signal ranging from 0 to 5 volts on `Dev1/ao0` and simultaneously reads the resulting signal from `Dev1/ai0`, displaying the input voltage in real-time.

## Troubleshooting:
- Ensure that the NI-DAQmx driver is installed and properly configured.
- Verify that the device (e.g., NI-USB-6008 or NI-USB-6009) is recognized by the system and the correct channels are selected.

## Code:
![image](https://github.com/user-attachments/assets/2bc982a4-1d86-44f2-aa5e-23e17a163e54)
