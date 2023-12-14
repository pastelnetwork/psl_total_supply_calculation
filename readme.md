# PSL Total Supply Calculation Project

## Introduction

This project is designed to calculate the total supply of Pastel coins (PSL) by iterating through all blocks in the Pastel blockchain and summing the block rewards. The script is asynchronous, utilizing `aiohttp` and `httpx` for efficient network communication.

## Prerequisites

Before you begin, ensure you have the following:

- Python 3.x installed on your machine
- Access to a Pastel node with RPC enabled

## Installation

To set up the project, follow these steps:

1. **Clone the Repository:**
   First, clone the repository to your local machine using Git:

   ```bash
   git clone https://github.com/pastelnetwork/psl_total_supply_calculation
   ```

2. **Create a Virtual Environment:**
   Navigate to the cloned directory and create a Python virtual environment. This isolates the project dependencies from your global Python environment.

   ```bash
   cd psl_total_supply_calculation
   python3 -m venv venv
   ```

3. **Activate the Virtual Environment:**
   To activate the virtual environment and use its packages, run the following:

   ```bash
   source venv/bin/activate
   ```

4. **Upgrade pip and Install wheel:**
   Upgrade `pip` to its latest version and install `wheel` for building packages.

   ```bash
   python3 -m pip install --upgrade pip
   python3 -m pip install wheel
   ```

5. **Install Dependencies:**
   Install the project dependencies using the provided `requirements.txt` file.

   ```bash
   pip install -r requirements.txt
   ```

## Configuration

To successfully connect to your Pastel node, ensure that the `pastel.conf` file is correctly set up with the following parameters:

- `rpcuser`: Your RPC username
- `rpcpassword`: Your RPC password
- `rpcport`: The port on which your node's RPC server is running

The script will automatically read these settings from the `pastel.conf` file located in your `~/.pastel/` directory.

## Running the Script

With the setup complete, you can now run the script to calculate the total PSL supply:

```bash
python3 psl_total_supply_calculation.py
```

The script will output log messages indicating the progress and the calculated total coin supply.

## Notes

- The script will take time to process all blocks, depending on the blockchain size and network speed.
- Ensure your Pastel node is fully synchronized with the blockchain before running the script.

## Troubleshooting

If you encounter any issues:

- Verify that your Pastel node is running and properly configured.
- Check that the RPC settings in `pastel.conf` match those expected by the script.
- Ensure your Python environment has all the required dependencies installed.

---

By following these instructions, you should be able to set up and run the PSL Total Supply Calculation project successfully.