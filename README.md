# Wireshark Packet Analysis

This Python script reads a Wireshark pcapng file and extracts statistics from the packet data. The script uses the `pyshark` library to parse the pcapng file, and `pandas` and `scipy` for data manipulation and statistical calculations.

## Features

- Extracts packet data such as source and destination IPs, ports, timestamps, packet lengths, and inter-arrival times.
- Groups the data by source and destination IPs and calculates statistics for each group, including variance, standard deviation, mean, median, mode, skew from median, skew from mode, and coefficient of variation for packet lengths and inter-arrival times.
- Calculates the total duration, total bytes sent and received, and the send and receive rates for each flow.
- Calculates response time statistics for each flow.
- Saves the resulting data to a CSV file.

## Requirements

- Python 3
- pyshark
- pandas
- scipy

## Usage

1. Install the required Python libraries with pip:

```bash
pip install -r .\requirements.txt
```

2. Capture the needed traffic for analysis and save the file in the same directory as the script, with name `wireshark_capture.pcapng`

3. Script output will be generated as `output.csv`

## Note
This script process TCP and UDP packets only. Other types of packets are not processed.