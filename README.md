# Simple Packet Sniffer 📡

This project is a **simple packet sniffer** built in Python, designed to monitor and decode incoming packets on a specified network interface. It provides detailed insights into network traffic by decoding various network protocols and displaying the packet details in real time.

## Project Overview

The packet sniffer captures Ethernet frames on a network interface and decodes layers such as Ethernet, IP, TCP, UDP, ICMP, and more. The output can be displayed on the screen, providing real-time insights into network activity.

## Features

- **Protocol Decoding**: Decodes Ethernet, IP, TCP, UDP, ARP, and ICMP protocols.
- **Modular Structure**: Built with classes to handle packet decoding and output for ease of extension.
- **Real-Time Monitoring**: Displays captured packet details in real time with optional data display.
- **Screen Output**: Uses a customizable output class to display packet details on the screen.

## Files in this Project

- **`core.py`**: Contains the `Decoder` and `PacketSniffer` classes, responsible for capturing and decoding packets.
- **`output.py`**: Defines the `OutputToScreen` class for displaying packet details.
- **`sniffer.py`**: Main script to start the packet sniffer, parse command-line arguments, and manage the packet capturing process.
- **`build.py`**: Script to build a standalone binary using PyInstaller.
- **`.gitignore`**: Excludes unnecessary files and directories from version control.
- **`requirements.txt`**: Lists dependencies required for the project.

## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Gitcomplex/packet-sniffer.git
   cd packet-sniffer
   ```

````
2. **Install Dependencies**: Make sure you have Python installed, then install the required
  packages:

```bash
 pip install -r requirements.txt
````

3. **Run the Sniffer**: To run the sniffer, use the following command:

```bash
 sudo python sniffer.py -i <interface> -d
```

Replace <interface> with your network interface (e.g., eth0). Use the -d flag to display packet data.

## Usage

The sniffer.py script accepts the following command-line arguments:

    -i or --interface: Specifies the network interface for capturing packets (defaults to all interfaces).
    -d or --data: Outputs captured packet data in addition to packet headers.

## Example:

```bash
  sudo python sniffer.py -i eth0 -d
```

- Building the Binary
- To build a standalone binary for the packet sniffer, run the following command:

```bash
  python build.py
```

- This uses PyInstaller to create a single executable file.

## Disclaimer

This packet sniffer is intended for educational and authorized testing purposes only. Unauthorized use of this software to monitor or capture network traffic on networks you do not own or have permission to access is strictly prohibited and may be illegal. Always ensure you have the necessary permissions before running this tool.
