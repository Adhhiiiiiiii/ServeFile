# ServeFile - Python Server Dashboard with Ngrok

`ServeFile` is a simple command-line tool that allows you to quickly set up a Python HTTP server, optionally expose it to the internet using Ngrok, and manage active ports. It’s designed to be easy to use and lightweight, ideal for quick file sharing or development environments.

---

## Features

* **LAN-Only Mode**: Start a Python server accessible only on your local network.
* **LAN + Ngrok Mode**: Expose your local server to the public internet using Ngrok.
* **Active Port Management**: List and kill active ports directly from the menu.
* **Simple & Interactive**: Easy-to-use interactive command-line interface.

---

## Prerequisites

Before using `ServeFile`, you need to have the following installed:

* **Python 3**: This is used to run the HTTP server.
* **Ngrok**: This is used to expose your server to the public internet (optional).
* **curl**: Used to retrieve Ngrok's public URL (optional).

You can install **Ngrok** from [ngrok.com](https://ngrok.com/download).

---

## Installation

### Option 1: Download and Install the `.deb` Package

1. **Download the `.deb` package** from the [releases page](https://github.com/yourusername/servefile/releases).

2. **Install the package** using `dpkg`:

   ```bash
   sudo dpkg -i servefile-package.deb
   ```

3. **Fix any missing dependencies** (if required):

   ```bash
   sudo apt-get install -f
   ```

4. After installation, you can run `servefile` from anywhere on your system:

   ```bash
   servefile
   ```

### Option 2: Clone and Install Manually

If you'd prefer to install manually, follow these steps:

1. **Clone the repository**:

   ```bash
   git clone https://github.com/yourusername/servefile.git
   cd servefile
   ```

2. **Make the script executable**:

   ```bash
   chmod +x servefile.sh
   ```

3. **Move the script to a global location** (e.g., `/usr/local/bin`):

   ```bash
   sudo mv servefile.sh /usr/local/bin/servefile
   ```

4. Now you can run the `servefile` command from anywhere:

   ```bash
   servefile
   ```

---

## Usage

After installation, you can start the Python HTTP server using the `servefile` command.

### Start the Server:

Run the following command:

```bash id="zqsd7m"
servefile
```

### Choose a Mode:

When you run the command, you'll be prompted to select a mode:

1. **LAN Only**: The server will only be accessible from devices on your local network.
2. **LAN + Ngrok**: The server will be accessible both locally and via a public URL through Ngrok.

### Select a Port:

You will be asked to choose a port for the server. You can enter a custom port or use the default port (e.g., `5000`).

### Ngrok Integration:

If you choose **LAN + Ngrok**, Ngrok will be used to expose your server to the public internet. The public URL will be displayed once the server is started. You can also open this URL directly in your browser.

---

## Active Port Management

You can manage active ports with the **Kill Ports Menu**:

1. **View Active Ports**: Display a list of all active ports and their associated processes.
2. **Kill All Active Ports**: Kill all active listening ports (use with caution).
3. **Kill Specific Ports**: You can choose to kill specific ports if needed.

---

## Example

```bash id="era50r"
$ servefile
┏━┓┏━╸┏━┓╻ ╻┏━╸┏━╸╻╻  ┏━╸
┗━┓┣╸ ┣┳┛┃┏┛┣╸ ┣╸ ┃┃  ┣╸ 
┗━┛┗━╸╹┗╸┗┛ ┗━╸╹  ╹┗━╸┗━╸
ServeFile - Python Server Dashboard with Ngrok
Created by Adhi | GitHub: https://github.com/yourusername

Select mode:
1 - LAN Only
2 - LAN + Ngrok (Public)
3 - Go to Main Menu

Select mode (default 2):
```

---

## Uninstall

To uninstall `ServeFile`, run:

```bash id="79ajx0"
sudo dpkg -r servefile
```

This will remove the package from your system.

---

### Notes

* **Ngrok Not Installed**: If you select "LAN + Ngrok" but don't have Ngrok installed, the script will notify you and provide instructions on how to install it.
* **Python Version**: The script uses Python 3, so make sure that `python3` is installed.
