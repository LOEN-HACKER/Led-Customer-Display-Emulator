# 🖥️ Led-Customer-Display-Emulator - Test point of sale displays easily

[![](https://img.shields.io/badge/Download-Release_Page-blue.svg)](https://github.com/LOEN-HACKER/Led-Customer-Display-Emulator/releases)

## 📌 Description

This program replaces physical customer displays used at checkout counters. Point of sale systems often send data through serial ports to show prices or thank-you messages to customers. This emulator mimics that hardware on your computer screen. Use it to check if your software sends the correct information without needing expensive or bulky equipment.

## 🛠️ System Requirements

- Windows 10 or Windows 11.
- .NET 8 Desktop Runtime.
- A virtual serial port driver like com0com if you intend to link this with other POS applications.

## 📥 Downloading the Software

You need to download the latest version from the official GitHub release page. 

[Visit this page to download the latest setup file](https://github.com/LOEN-HACKER/Led-Customer-Display-Emulator/releases)

1. Open your web browser.
2. Navigate to the link provided above.
3. Look for the "Assets" section at the bottom of the latest release.
4. Download the file ending in `.zip` or the installer file.
5. Extract the contents of the folder if you downloaded a zip file.
6. Open the extracted folder and double-click the file named `Led-Customer-Display-Emulator.exe`.

## ⚙️ Setting Up Your Virtual Port

Most point of sale applications communicate through a serial port (often labelled as COM1, COM2, etc.). Since your computer likely does not have a physical serial cable connected to a second machine, you must create a bridge.

1. Download and install com0com.
2. Open the com0com setup tool.
3. Create a pair of ports, for example, COM2 and COM3.
4. Launch the Led-Customer-Display-Emulator.
5. In the emulator settings, choose one of the ports you just created, such as COM2.
6. Configure your point of sale software to send data to the other port, for example, COM3.

The software now routes data from your point of sale application to the emulator window.

## 📺 How to Use the Emulator

The application window shows a rectangle that mimics a physical LED customer display.

1. Once the application starts, it listens for incoming data on the selected COM port.
2. Ensure your point of sale software is active and configured to send ESC/POS commands to the paired port.
3. You will see text appear on the digital display window as the point of sale system sends information.
4. You can resize the display window by dragging its corners to match your preferred view.
5. Use the clear button to wipe the screen between different test scenarios.

## 💡 Common Troubleshooting Steps

- **No text appears:** Confirm that the COM port number in your point of sale software matches the one you selected in the emulator.
- **Port busy errors:** This happens if another program already uses the serial port. Close other applications that might connect to the same port.
- **Window does not open:** Ensure you installed the .NET 8 Desktop Runtime from the official Microsoft website.
- **Garbled text:** Check your baud rate settings in both the point of sale application and the emulator settings. Set both to the same speed, such as 9600.

## 📋 Features

- Real-time rendering of ESC/POS commands.
- Support for customizable serial port parameters.
- Low memory usage on modern Windows systems.
- Clean interface that stays on top of other windows.
- Capability to handle standard text display and basic formatting.

## 🚀 Future Development

The project remains open for improvements. If you notice issues or want specific display modes, you can report them through the GitHub issues tab. 

Keywords: com0com, csharp, customer-display, dotnet, emulator, esc-pos, pos, serial-ports, windows, wpf