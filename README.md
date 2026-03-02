
# Embedded-System-Assignment

Here is a requirements document for a **Calculator with keypad and LCD**:

---

# Calculator with keypad and LCD RFID

## **1. Introduction**

### **1.1 Purpose**



### **1.2 Scope**

The system will:

* 
* 
* 
* 

---

## **2. Functional Requirements**

### **2.1 Student Registration and Tag Assignment**

* 
* 

### **2.2 Attendance Detection via RFID**

* 
* 

### **2.3 Teacher/Admin Interface**

* 
* 
* 

### **2.4 Real-time Notifications**

* 
  
### **2.5 Excel Database**

* 


---

## **3. Non-Functional Requirements**

### **3.1 Performance**

* 
* 
*

### **3.3 Reliability and Availability**

* 
* 

### **3.4 Maintainability and Scalability**

* 
* 

---

## **4. Hardware and Software Requirements**

### **4.1 Hardware Requirements**

| Component                       | Description                                                          |
| ------------------------------- | -------------------------------------------------------------------- |
| **Microcontroller Unit (MCU)**  | ESP32 / Arduino Uno / STM32 to interface with RFID reader and server |
| **RFID Reader Module**          | MFRC522 or compatible HF reader for scanning RFID tags               |
| **RFID Tags**                   | Passive RFID cards (13.56 MHz), one per student                      |
| **OLED/LCD Display (Optional)** | Display attendance status or messages to student/teacher             |
| **Buzzer / LED**                | Signal success or failure during scanning                            |
| **Push Buttons**                | Manual override, reset, or mode switching (optional)                 |
| **Wi-Fi or Ethernet Module**    | Built-in (ESP32) or external module for communication with server    |
| **Power Supply**                | 5V power supply for MCU and reader module, 12V battery                       |

---

### **4.2 Software Requirements**

| Software Component       | Description                                                               |
| ------------------------ | ------------------------------------------------------------------------- |
| **Embedded Firmware**    | Code to control RFID reader, read tags, and send data via serial or Wi-Fi |
| **Database System**      | MySQL / PostgreSQL to store attendance records and student info           |
| **Web Server / Backend** | Python Flask / Node.js / PHP to receive data and serve dashboard          |
| **Admin Dashboard**      | Web interface for teachers/admin to view reports and student records      |
| **Notification Module**  | Optional integration with email (SMTP) or SMS (Twilio/Firebase) APIs      |
| **Driver Libraries**     | RFID and Wi-Fi libraries compatible with the chosen microcontroller       |

---

## **5. Assumptions and Constraints**

* Each student must carry their assigned RFID tag during class time.
* RFID readers must be installed and powered near classroom entrances.
* The system assumes that only one student enters at a time for accurate scan.
* A stable **Wi-Fi or LAN connection** is required for real-time data sync and notifications.
* The RFID reader’s range is assumed to be **<10 cm** to prevent misreads.
* The school must ensure physical security of hardware to prevent tampering.

---
# Embedded-Assignment-Attendance-check-in-using-ESP32-Controlled-RFID
# Embedded-Assignment-Attendance-check-in-using-ESP32-Controlled-RFID
# Embedded-Assignment-Attendance-check-in-using-ESP32-Controlled-RFID
