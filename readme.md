# Network Scanner Suite

This project is a network scanning toolset that performs subnet scanning, port scanning, and operating system fingerprinting. It is composed of three Python scripts working in form of a chain: `scanner.py`, `ping_and_port_scan.py`, and `os_fingerprint.py`.

## Features
- **Ping Sweep**: Identifies live hosts within a given subnet and netmask.
- **Port Scanning**: Scans common ports (1–1023 by default) on live hosts.
- **OS Fingerprinting**: Detects the operating system and other details for each live host with open ports.
- **Output to CSV**: Saves scan results in a CSV file for easy analysis.

---

## File Descriptions

### `scanner.py`
The main script to run the network scanning process.

- **Functions**:
  - Accepts subnet and mask as command-line arguments.
  - Performs a ping sweep to find live hosts.
  - Scans for open ports on each live host.
  - Uses the `os_fingerprint.py` script for OS detection and detailed scanning.
  - Saves the results in a CSV file named `scan_results.csv`.

- **Usage**:
    ```bash
    python scanner.py <subnet> <mask>
    ```
    
    ```python
    python scanner.py 192.168.1.0 24
    ```


