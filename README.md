Key Components and Modules
Raspberry Pi: Serves as the central computing unit, hosting and executing all software components and managing communication with hardware peripherals.

HX711 Handling: Dedicated to managing interactions with the HX711 chip used for weight measurement. This module includes Python classes for initializing the chip, reading and processing data, and utilities for calibration and weight measurement.

Protocol Management: Responsible for controlling and monitoring hardware components through I2C and GPIO interfaces. This includes setting up GPIO pins, managing I2C communication, and handling serial communication with Arduino boards.

User Interface (UI): Developed using PyQt5, this module focuses on providing a graphical user interface for the application. It integrates video playback functionality and configuration management, offering a user-friendly way to interact with the application.

Configuration & Communication: Manages application settings through configuration files and facilitates serial communication with external devices like Arduino boards. This module is crucial for customizing the application to meet specific user or environment requirements.

Video Playback: Utilizes PyQt5 multimedia modules to offer video playback capabilities within the application's UI. This includes basic operations such as play, pause, and stop, enhancing the user experience with multimedia content.

Directory Structure and Important Files
The application's codebase is organized in a manner that reflects its modular architecture. Key directories and files include:

HX711-master/HX711_Python3/ and hx711py-master/: Contain the Python classes and utilities for HX711 handling.
videoplayer.py: Implements the video playback functionality using PyQt5 multimedia modules.
The root directory (.): Hosts the main application files, including those for protocol management, UI, and configuration & communication.
Architectural Invariants
Separation of Concerns: Each major functionality (e.g., HX711 handling, UI) is encapsulated within its own module, ensuring that changes to one module have minimal impact on others.
Hardware Abstraction: The application abstracts the hardware layer from the software through the Protocol Management and HX711 Handling modules, allowing for easier adaptation to different hardware components.
Configurability: Through the Configuration & Communication module, the application can be easily customized without altering the core codebase, adhering to the principle of flexibility and extensibility.
Boundaries and Interfaces
Hardware-Software Interface: Defined by the Protocol Management module, this boundary abstracts the hardware details from the software, providing a clean interface for software components to interact with hardware peripherals.
UI and Core Logic Separation: The UI module interacts with the core logic through well-defined interfaces, ensuring that the UI can evolve independently of the core application logic.
