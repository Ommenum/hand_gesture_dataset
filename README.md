# hand_gesture_dataset


S21 hand‑reflection data using a ZNA43, horn antennas, and a RIS.

A link to the data is provided:
https://drive.google.com/drive/folders/19n-p1ufx06bDIAidp1X9wfeMW5GRE3tY?usp=sharing

# Data Collection Procedure

The measurement data in this repository is collected using a Rohde & Schwarz ZNA43 vector network analyzer (VNA) controlled through Python via PyVISA. The measurement setup consists of two horn antennas and a reconfigurable intelligent surface (RIS). The script configures the VNA to measure the S21 parameter over a frequency range of 4.8–5.2 GHz using 1000 sweep points.

For each measurement, the user manually triggers a sweep by pressing ENTER. This allows the measurement conditions to be adjusted between samples, such as repositioning a hand or changing the RIS configuration. When a sweep is triggered, the VNA returns the complex S21 data along with the corresponding frequency points.

The script converts the complex S21 values into amplitude (in dB) and phase (in degrees). Each measurement is stored as a single row containing 3000 values: 1000 amplitude values, 1000 phase values, and 1000 frequency values. After all measurements are completed, the script generates a CSV file containing the full dataset, including a header describing the column structure and a timestamp indicating when the data was recorded.
