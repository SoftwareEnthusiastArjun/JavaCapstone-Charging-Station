Charging Station Management System:
==================================
  This Java program simulates a charging station management system for electric vehicles. The system includes classes to represent charging stations, cars, admins, and file handling functionalities. The project documentation includes comprehensive UML diagrams depicting the system's activities, use cases, and state transitions. Below is an overview of the key components and functionalities of the program:


Components:
============
Admin Class:
------------
Represents an admin user with an ID, password, and association with a charging station.

TC (Time Checker) Class:
------------------------
Extends Thread and is responsible for checking the waiting time of cars in the waiting list of a charging station.
If a car waits too long without getting a slot, it leaves without charging.

ChargingStation Class:
-----------------------
Manages a charging station with attributes such as ID, location, total slots, available slots, waiting list of cars, and file writers for logging.
Implements methods to book and release charging slots, handle waiting list, and assign energy sources (solar, wind, or power grid) to charging sessions.

Car Class:
----------
Represents an electric car with an ID, location, charging duration, and an array of available charging stations.
Finds the nearest charging station based on location and initiates a charging session.

DirCreator Class:
-----------------
Creates directories based on specified names.

FileCreator Class:
-------------------
Creates files within specified directories.

Functionalities:
=================
Charging Station Management:
------------------------------
Allows booking and releasing of charging slots for electric cars.
Manages waiting lists for cars when no slots are available.

Energy Source Assignment:
-------------------------
Randomly assigns solar, wind, or power grid as the energy source for charging sessions.

File Handling:
--------------
Creates directories (StationLogFiles, Date_Wise, Solar, Wind, Grid) and corresponding log files for recording charging activities.
Logs charging details including car ID, charging duration, station ID, and energy source used.

User Interaction:
----------------
Provides a command-line interface for users to view and interact with log files.
Supports viewing station log files, energy source log files, and date-wise log files.
Implements basic authentication for admin users to access specific log files.

Test Cases:
===========
The project includes comprehensive test cases to ensure the correctness of the charging station management system. Key test cases include:

Finding Nearest Station:
-------------------------
Validates if cars correctly identify the nearest charging station based on their location.

Energy Source Assignment:
------------------------
Verifies that energy sources (solar, wind, power grid) are assigned correctly within a valid range.

File Creation:
--------------
Tests the creation of directories and files, ensuring that they are created successfully and exist.

Admin Authorization:
--------------------
Checks if admin credentials are correctly validated for accessing specific functionalities.

Thread Synchronization:
----------------------
Tests thread synchronization to ensure proper management of charging slots and waiting lists.

Directory Creation:
-------------------
Validates the creation of directories for storing log files.

Running the Program:
====================
Setup:
-----
Compile and run the Main class to execute the charging station management system.

Interaction:
------------
Follow the prompts in the console to view log files and perform actions such as file deletion based on user input.
