Arduino Leonardo Cybersecurity Project: WiFi Password Extraction

Overview:

This project demonstrates the capabilities of the Arduino Leonardo microcontroller, specifically utilizing its ability to emulate a USB keyboard and interact with a target system. By leveraging PowerShell commands, the Arduino can extract stored WiFi credentials (SSIDs and passwords) from a victim’s system and store the data in its EEPROM. Once the data is captured, it can be retrieved by connecting the Arduino to another system.

This project serves as an experimental demonstration of the interaction between hardware and software in the context of cybersecurity. It is important to note that this project should only be used for ethical purposes and with explicit permission.

Components Used:
Arduino Leonardo: A microcontroller with built-in USB communication capabilities.
2 Push Buttons: Used to trigger data extraction and data retrieval.
PowerShell: A scripting language for executing commands on the target system.
EEPROM: Non-volatile memory on the Arduino used to store extracted data.

How It Works:
Setup:

Connect the Arduino Leonardo to the victim’s computer via USB.
When the left button is pressed:
The Arduino emulates a keyboard and launches the PowerShell terminal.
PowerShell commands are executed to extract WiFi SSIDs and passwords from the system.
The extracted data is saved in the Arduino’s EEPROM (which retains the data even when powered off).
Data Retrieval:

After the data is captured, disconnect the Arduino from the victim’s computer.
Connect the Arduino to your own system.
When the right button is pressed:
The stored data from the EEPROM is retrieved and dumped onto your system via the serial connection.
Code Explanation
extractingData() function:
Launches PowerShell.
Executes a command to retrieve WiFi credentials stored on the system.
Saves the extracted data into the Arduino’s EEPROM.
dispatchingData() function:
Opens Notepad (on the target system).
Dumps the stored WiFi credentials (from EEPROM) into Notepad for easy viewing.

Requirements:
Arduino IDE: To upload the sketch to the Arduino.
Arduino Leonardo: Microcontroller board for USB communication.
PowerShell: To execute commands on the target system (Windows).
Two Push Buttons: Connected to the Arduino for triggering actions.

Ethical Considerations:
This project is intended for educational and experimental purposes only. It demonstrates how small, low-cost devices like the Arduino Leonardo can interact with systems to perform tasks that could have serious security implications if misused. Always obtain explicit permission before using this on any system or network.

License
This project is licensed under the MIT License. See the LICENSE file for more information.

Contact
If you have any questions or suggestions, feel free to reach out to me via my GitHub profile.

