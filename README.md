
# Embedded-System-Assignment

Here is a requirements document for a **Calculator with keypad and LCD**:

---

# Calculator with keypad and LCD 

## **1. Introduction**

### **1.1 Purpose**
The purpose of our project is to design and develop a basic and functional calculator system using a microcontroller, integrated with a keypad for user input and an LCD for output display. The system aims to perform basic arithmetic operations such as addition, subtraction, multiplication, and division in a reliable and efficient manner.

Additionally, this project serves as a practical application of embedded systems design, focusing on the integration of hardware components (keypad, LCD, and microcontroller) with software control. It also helps us in understanding communication protocols (such as GPIO or I2C), real-time data processing, and user interface implementation in resource-constrained environments.

### **1.2 Scope**

The system will:

* Design and implementation of a standalone calculator system based on a microcontroller
* Development of hardware schematic, including keypad and LCD interfacing
* Implementation of keypad input using matrix scanning techniques
* Integration of LCD module for displaying user input and calculation results
* Development of embedded firmware for performing basic arithmetic operations
* Testing and validation of system functionality under normal operating conditions
  
---

## **2. Functional Requirements**

### **2.1 Input Handling Requirements**

* FR-01 (High): The system shall accept user input via a matrix keypad.
* FR-02 (High): The system shall detect and register each key press accurately.
* FR-03 (High): The system shall support numeric inputs ranging from 0 to 9.
* FR-04 (High): The system shall support arithmetic operators including addition (+), subtraction (−), multiplication (×), and division (÷).
* FR-05 (Medium): The system shall provide function keys including “equals (=)” and “clear (C)”.

### **2.2 Processing Requirements**

* FR-06 (High): The system shall process input data in real time.
* FR-07 (High): The system shall perform basic arithmetic operations: addition, subtraction, multiplication, and division.
* FR-08 (Medium): The system shall evaluate expressions based on the sequence of user input.
* FR-09 (High): The system shall handle division-by-zero conditions by displaying an appropriate error message.

### **2.3 Display Requirements**

* FR-10 (High): The system shall display user inputs on the LCD as they are entered.
* FR-11 (High): The system shall display the result of calculations clearly on the LCD.
* FR-12 (Medium): The system shall update the LCD display after each input or operation.

### **2.4 Control Requirements**

* FR-13 (High): The system shall provide a clear function to reset current input and results.
* FR-14 (High): The system shall initialize all system components upon power-up.
* FR-15 (Medium): The system shall maintain stable operation during continuous usage.
  
### **2.5 Error Handling Requirements**

* FR-16 (Medium): The system shall detect invalid inputs or unsupported operations.
* FR-17 (High): The system shall display appropriate error messages when an error occurs.
* FR-18 (Medium): The system shall allow the user to recover from errors using the clear function.

---

## **3. Non-Functional Requirements**

### **3.1 Performance**

* NFR-01 (High): The system shall respond to each key press within 100 ms.
* NFR-02 (High): The system shall display computation results immediately after the equals (=) operation is triggered.
* NFR-03 (Medium): The system shall handle continuous input without noticeable delay. 

### **3.2 Reliability and Availability**

* NFR-04 (High): The system shall operate continuously without failure under normal usage conditions.
* NFR-05 (High): The system shall produce accurate results for all valid arithmetic operations.
* NFR-06 (Medium): The system shall recover safely from minor errors (e.g., invalid input) without requiring a restart.

### **3.3 Usability**

* NFR-07 (Medium): The system shall provide a clear and readable display on the LCD.
* NFR-08 (Medium): The keypad layout shall be intuitive and easy to use.
* NFR-09 (Low): The system shall provide simple user feedback (e.g., clearing display after reset).

### **3.4 Hardware Constraints**

* NFR-10 (High): The system shall operate using a microcontroller with limited processing and memory resources.
* NFR-11 (High): The system shall interface with the LCD and keypad using standard communication methods (e.g., GPIO or I2C).
* NFR-12 (Medium): The system shall maintain low power consumption suitable for embedded applications.

### **3.4 Maintainability Requirements**

* NFR-13 (Medium): The system firmware shall be modular and easy to modify.
* NFR-14 (Low): The system design shall allow future extension for additional features.

---

## **4. Hardware and Software Requirements**

### **4.1 Hardware Requirements**

| Component                       | Description                                                                         |
| ------------------------------- | ------------------------------------------------------------------------------------|
| **Microcontroller Unit (MCU)**  | STM32 used as the main processing unit for handling input, computation, and control |
| **Keypad (Matrix 5x5)**         | Used for user input (numbers and operators)                                         |                  
| **LCD Display**                 | Displays input data and calculation results                                         |                  
| **Power Supply**                | 5V regulated power supply for MCU and peripherals                                   |                  
| **Resistors / Capacitors**      | Supporting components for stable circuit operation                                  |                  
| **Crystal Oscillator**          | Provides accurate clock for MCU operation                                           |                  
| **Wi-Fi or Ethernet Module**    | Built-in (ESP32) or external module for communication with server                   |                  
| **Programming/Debug Interface** | SWD interface for firmware uploading and debugging                                  |                  

---

### **4.2 Software Requirements**

| Software Component       | Description                                                                         |
| --------------------------- | -------------------------------------------------------------------------------- |
| **Embedded Firmware**       | Main program running on the MCU to control system operations                     |
| **Keypad Driver**           | Handles matrix keypad scanning and key detection                                 |
| **LCD Driver (I2C/GPIO)**   | Controls LCD display and updates content                                         |
| **Input Processing Module** | Interprets user input (numbers and operators)                                    |
| **Calculation Module**      | Performs arithmetic operations (addition, subtraction, multiplication, division) |
| **Control Logic**           | Manages system flow (input → process → display)                                  |
| **Error Handling Module**   | Detects and handles errors (e.g., division by zero, invalid input)               |
| **Initialization Routine**  | Initializes system peripherals (GPIO, I2C, LCD) at startup                       |
| **Development Tools**       | IDE (e.g., STM32CubeIDE) and compiler for firmware development                   |
| **Driver Libraries**        | Wi-Fi libraries compatible with the chosen microcontroller                       |

---

## **5. Assumptions and Constraints**

### **5.1 Assumptions**

* The user has basic knowledge of operating a calculator device.
* The keypad inputs are valid and entered in a logical sequence.
* The power supply provided to the system is stable and within the required voltage range.
* The microcontroller operates under normal environmental conditions.
* The LCD module functions correctly and is compatible with the selected interface (GPIO/I2C).
* No external interference significantly affects keypad input or display output.

### **5.2 Constraints**

* Limited processing power and memory of the microcontroller.
* Restricted to basic arithmetic operations only.
* Limited display capability due to character-based LCD (e.g., 16x2).
* Hardware design must remain low-cost and simple.
* Limited number of I/O pins available for keypad and LCD interfacing.
* Power consumption must be kept low for embedded applications.
* Development time and resources are limited.

---
