# PPG-serial-monitor
 
![nn](/images/ppg_monitor.png)

# PPG Signal Monitor

A PyQt5-based application to display and record PPG (Photoplethysmogram) signals using STM32H750xB (CORTEX M7) microcontroller.

## Overview

This project interfaces with the **ART PI** development board (featuring the STM32H750xB microcontroller) and uses a serial connection to capture, visualize, and save PPG signals in real-time. The graphical user interface (GUI) enables users to:

- Monitor PPG signals in real-time.
- Adjust graph settings (e.g., X and Y axis range).
- Save PPG signal data and corresponding graphs.
- Process data to estimate metrics like BPM (Beats Per Minute).

## Features

- **Real-Time Signal Monitoring**: Visualize PPG and pulse signals using PyQtGraph.
- **Serial Communication**: Communicate with the STM32 board via serial ports.
- **Customizable Graphs**: Adjust graph ranges, channels, and display settings.
- **Data Recording and Saving**: Record and save PPG data to Excel and PNG files.
- **Signal Processing**: Calculate BPM and estimate SpO2 levels.

## Hardware Requirements

- **Development Board**: ART PI with STM32H750xB (CORTEX M7).
- **Debugger**: ST-Link v2 for flashing and debugging.
- **PPG Sensor**: Compatible sensor for PPG data acquisition.
- **Host System**: Windows, Linux, or macOS with Python installed.

## Software Requirements

- Python 3.8+
- Required Python libraries:
  ```
  pip install PyQt5 pyqtgraph pandas numpy matplotlib scipy pyserial
  ```
- STM32 development tools for setting up the ART PI board.

## Installation and Setup

1. **Clone the Repository**:
   ```
   git clone https://github.com/yourusername/ppg-signal-monitor.git
   cd ppg-signal-monitor
   ```

2. **Install Dependencies**:
   Use the provided `requirements.txt` file for easy installation:
   ```
   pip install -r requirements.txt
   ```

   Alternatively, manually install the required libraries:
   ```
   pip install PyQt5 pyqtgraph pandas numpy matplotlib scipy pyserial
   ```

3. **Connect Hardware**:
   - Connect the ART PI board to your host system via ST-Link and USB.
   - Ensure the PPG sensor is properly connected to the board.

4. **Run the Application**:
   Execute the Python script:
   ```
   python ppg_signal_monitor.py
   ```

## Usage

1. Launch the application.
2. Select the appropriate serial port and baud rate.
3. Click "Port Open" to establish a connection.
4. Click "Start" to begin monitoring PPG signals.
5. Adjust graph settings (X/Y axis ranges, channels, grid) as needed.
6. Click "Record" to start recording data and "Save" to export recorded signals.

## Graphical User Interface

- **PPG Signal Display**: Real-time plotting of PPG and pulse signals.
- **Serial Communication Panel**: Configure ports, baud rates, and sampling rates.
- **Settings Panel**: Adjust graph ranges, enable/disable channels, and save configurations.
- **Data Monitor**: Display raw and processed data (e.g., BPM and SpO2).

## File Outputs

- **PPG Graph**: Saved as `ppg_waves.png` in the specified directory.
- **Data Records**: Exported as an Excel file `data.xlsx` containing timestamped voltage values.

## Contribution

Contributions are welcome! Feel free to open issues or submit pull requests for bug fixes or feature additions.


## Author

**Ryuha Kim**  
Yonsei University

---


