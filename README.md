# Gesture-Based Embedded Air Mouse

An embedded systems project that transforms a physical microcontroller into a wearable, gesture-controlled computer mouse. By tracking hand tilts and wrist movements in real-time, this device translates physical motion directly into mouse cursor coordinates on a computer screen without requiring any external software or drivers.

## 🚀 How It Works
The project uses an Inertial Measurement Unit (IMU) to detect angular velocity and acceleration. The onboard microcontroller processes these physical movements using C++ algorithms, filters out minor hand tremors, and sends standard mouse movement signals to the connected PC over USB or Bluetooth.

## 🛠️ Hardware Requirements
* **Microcontroller:** HID-compliant development board (such as Arduino Leonardo, Micro, Pro Micro, or an ESP32/STM32 with USB/BLE capabilities) configured via Arduino IDE.
* **Motion Sensor:** MPU6050 6-Axis Gyroscope & Accelerometer module.
* **Buttons:** Tactile push buttons for Left Click and Right Click functionality.

## 💻 Technical Features & Implementation
* **Inertial Motion Tracking:** Reads raw X and Y-axis data from the gyroscope to track active hand rotation.
* **Signal Filtering & Smoothing:** Implements digital filtering algorithms in C++ to stabilize the cursor, eliminate sensor drift, and ensure smooth tracking across the screen.
* **Native HID Emulation:** Utilizes native Human Interface Device (HID) protocols, allowing the computer to recognize the device instantly as a plug-and-play USB mouse.

## 📁 Repository Structure
* `/Air_Mouse.ino` -> Core C++ firmware script containing sensor calibration, motion processing loop, and HID mouse execution.
* `/README.md` -> Project documentation and setup guide.
