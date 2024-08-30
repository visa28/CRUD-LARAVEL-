This repository contains the source code and setup instructions for a Google Smart Home IoT Project using a Raspberry Pi to control three lamps. The project integrates with Google Assistant, allowing users to control the lamps through voice commands. This project demonstrates how to create a smart home environment using affordable hardware and cloud-based services, providing users with convenience and enhancing their home automation experience.

Key Features:

Voice Control via Google Assistant: Users can turn the lamps on or off using voice commands through Google Assistant. This integration allows for hands-free control, making it more convenient for users to manage their lighting.
Raspberry Pi as a Hub: The Raspberry Pi serves as the central control hub, managing communication between the lamps and Google Assistant. It processes the commands received and sends the appropriate signals to control the lamps.
IoT Connectivity: The system connects the lamps to the internet, allowing for remote control through the Google Home app or via voice commands from anywhere with internet access.
Scalability: The setup can be easily expanded to control more devices or other types of appliances, providing a scalable solution for smart home automation.
Feedback Mechanism: The system provides feedback to the user through Google Assistant, confirming the status of the lamps (on/off).
Technology Stack:

Hardware:

Raspberry Pi: Acts as the main controller for the project. It runs the necessary scripts and handles communication with Google Assistant.
Relays: Connected to the Raspberry Pi’s GPIO pins, these relays control the power to each of the three lamps.
Lamps: Standard lamps connected to the relays, which can be turned on or off through the Raspberry Pi.
Software:

Python: Programming language used for writing the control scripts that run on the Raspberry Pi.
Google Assistant SDK: Used to integrate the Raspberry Pi with Google Assistant for voice control functionality.
Google Cloud Platform: Provides the backend infrastructure for handling voice commands and integrating with Google Assistant.
MQTT Protocol: An optional lightweight messaging protocol that can be used for communication between devices and the Raspberry Pi.
How it Works:

Setup and Configuration:

Raspberry Pi Configuration: The Raspberry Pi is set up with Raspbian OS and configured with the Google Assistant SDK. Necessary Python libraries and tools are installed to enable control over the GPIO pins.
Google Cloud Platform: A project is set up on Google Cloud, and the Raspberry Pi is authenticated as a device to communicate with Google Assistant. APIs and credentials are configured to allow secure communication.
Voice Command Processing:

When the user gives a voice command, such as "Turn on lamp 1," Google Assistant processes the command and sends it to the Raspberry Pi via the Google Cloud Platform.
The Raspberry Pi receives the command, and a Python script maps the voice command to the appropriate GPIO pin, which is connected to the corresponding relay controlling the lamp.
Lamp Control:

The Raspberry Pi sends a signal to the relay, which either turns the lamp on or off based on the user’s command.
For example, a command to "Turn on all lamps" would send signals to all three relays, activating all three lamps simultaneously.
Feedback to User:

After executing the command, the Raspberry Pi sends a confirmation back to Google Assistant. Google Assistant then provides verbal feedback to the user, confirming the action, such as "Lamp 1 is now on."
Remote Control via Google Home App:

Users can also control the lamps through the Google Home app, providing a graphical interface for managing the lighting setup. This app syncs with Google Assistant and the Raspberry Pi to control the lamps remotely.
Expandability:

The system is designed to be modular and scalable, allowing additional lamps or other appliances to be added easily by configuring more GPIO pins and relays. Additional voice commands can be programmed to handle these new devices.
