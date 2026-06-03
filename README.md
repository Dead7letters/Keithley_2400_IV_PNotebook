# Keithley 2400 Current vs Time Measurement

## Overview

This Jupyter Notebook controls a Keithley 2400 SourceMeter using PyVISA to measure current as a function of time under a constant voltage bias.

The notebook:

* Connects to a Keithley 2400 via GPIB
* Applies a user-defined voltage bias
* Measures current at regular time intervals
* Displays a real-time current vs time plot
* Saves measurement data to a CSV file
* Automatically disables the output when the measurement is complete

---

## Requirements

### Hardware

* Keithley 2400 SourceMeter
* GPIB interface (NI GPIB-USB-HS or equivalent)
* Computer running Python/Jupyter Notebook

### Software

* Python 3
* PyVISA
* NI-VISA or Keysight VISA
* NumPy
* Matplotlib

Install required packages:

```bash
pip install pyvisa numpy matplotlib
```

---

## User Inputs

The following parameters can be adjusted in the notebook:

| Parameter            | Description                    |
| -------------------- | ------------------------------ |
| `bias_voltage`       | Applied voltage bias (V)       |
| `total_time_s`       | Total measurement duration (s) |
| `sample_interval_s`  | Time between measurements (s)  |
| `current_compliance` | Maximum allowed current (A)    |
| `save_filename`      | Output CSV filename            |

---

## Output

The notebook generates:

### Real-Time Plot

Current (A) vs Time (s)

### CSV File

Columns:

```text
Time_s
Voltage_V
Current_A
Bias_Setpoint_V
Current_Compliance_A
```

---

## Safety Notes

* Always set an appropriate current compliance before enabling the output.
* Verify the voltage bias is safe for the device under test.
* The notebook automatically turns the Keithley output OFF at the end of the measurement.
* An emergency shutdown cell is included for manual output disable.

---

## Typical Use

1. Connect the Keithley 2400.
2. Run the connection cell.
3. Set measurement parameters.
4. Run the measurement cell.
5. Watch the real-time plot update.
6. Save the data to CSV.
7. Turn off the output when finished.

---

## Shlok Joseph Paul 2026

Custom Jupyter Notebook for Keithley 2400 automated current-vs-time measurements.
