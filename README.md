# Optimizing Urban Transit: Adaptive and Inclusive Seating Allocation Strategies
## 📌 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [System Architecture](#system-architecture)
- [Dataset Description](#dataset-description)
- [Installation](#installation)
- [Usage](#usage)
- [Project Workflow](#project-workflow)
- [Sample Outputs](#sample-outputs)
- [Evaluation Metrics](#evaluation-metrics)
- [Future Enhancements](#future-enhancements)
- [Published Paper](#-published-paper)
- [Team Members](#team-members-amrita-school-of-computing-bengaluru)
- [Mentor](#-mentor)
- [Acknowledgment](#-acknowledgment)


## Overview
This project presents an innovative Smart Adaptive Seating Allocation System for urban transit that enhances passenger comfort and safety. Leveraging priority queue algorithms, the system dynamically assigns seats based on passenger needs including age, pregnancy status, and medical conditions. The Java-based Metro App for Bangalore Metro combines advanced graph algorithms for route optimization with intelligent seating allocation, handling both Purple and Green metro lines with seamless interchange management and health-conscious arrangements.

## Features
- **Route Planning**: Find shortest paths between 62 metro stations across Purple and Green lines
- **Distance & Time Calculation**: Calculate optimal routes based on distance or travel time
- **Intelligent Seat Allocation**: Priority-based seating with health safety considerations
- **Interchange Detection**: Automatic handling of line changes at Majestic station
- **Multi-input Support**: Station selection via serial numbers, codes, or full names
- **Health-conscious Design**: Separate seating zones for infectious and susceptible passengers
- **Special Needs Priority**: Dedicated support for disabled, elderly, and pregnant passengers

## Technologies Used
- **Programming Language**: Java 8+
- **Data Structures**: Custom Generic Heap, HashMap, ArrayList, LinkedList
- **Algorithms**: Dijkstra's Algorithm, Custom Heap Implementation, Graph Traversal
- **Architecture**: Object-Oriented Programming with Generic Classes and modular design

## System Architecture
### Core Components
- **Graph_M Class** (`Graph_M.java`): Metro network representation using weighted graphs with custom heap for optimization
- **Heap Class** (`Heap.java`): Generic priority queue implementation with HashMap indexing for O(log n) operations
- **Metro_seats Class**: 50-seat metro car simulation with zone-based allocation
- **Seat Class**: Individual seat properties (AC proximity, door access)
- **Passenger Class**: Passenger information and health status management

### Key Technical Features
- **Custom Generic Heap**: Implements priority queue with updatePriority() functionality
- **Hash-based Indexing**: O(1) element lookup in heap using HashMap mapping  
- **Dynamic Priority Updates**: Real-time priority adjustments for Dijkstra's algorithm
- **Generic Design**: Type-safe implementation supporting any Comparable objects
- **Modular Architecture**: Separate files for heap implementation and graph operations

### Network Coverage
- **Purple Line**: 35 stations (Whitefield ↔ Challaghatta)
- **Green Line**: 27 stations (Nagasandra ↔ Silk Institute)
- **Interchange**: Majestic (Nadaprabhu Kempegowda Station)

## Dataset Description
The application uses a comprehensive dataset of Bangalore Metro stations including:
- Station names and codes for both Purple and Green lines
- Inter-station distances and connection mappings  
- Travel time estimates with interchange delays
- Seat configuration data for metro cars
- Zone classifications for different passenger categories
- Priority-based data structures for efficient route calculation using custom heap implementation

## Installation
1. **Prerequisites**: Java 8 or higher installed
2. **Download**: Clone or download the project files
3. **Compile**: 
   ```bash
   javac Heap.java
   javac Graph_M.java
   ```
4. **Run**: `java Graph_M`

## Usage
### Menu Options
1. List All Stations
2. Show Metro Map
3. Calculate Shortest Distance
4. Calculate Shortest Time
5. Find Shortest Path (Distance-based)
6. Find Shortest Path (Time-based)
7. Seat Allocation System
8. Exit Application

### Input Examples
- **Route Planning**: `Whitefield~P` to `Silk Institute~G`
- **Seat Allocation**: Enter passenger details including health status and special needs

## Project Workflow
1. **Heap Initialization**: Custom generic heap (Heap.java) provides efficient priority queue operations
2. **Network Construction**: Metro network setup in Graph_M.java using the custom heap for Dijkstra's algorithm
3. **User Input Processing**: Handle multiple input formats for station selection
4. **Route Calculation**: Apply Dijkstra's algorithm with custom heap for optimal path finding
5. **Priority Management**: Use updatePriority() method for dynamic distance updates during graph traversal
6. **Seat Assignment**: Process passenger priorities and allocate seats accordingly
7. **Output Generation**: Display routes, distances, times, and seat arrangements

## Sample Outputs
### Route Planning
```
Source: Whitefield (Purple Line)
Destination: Silk Institute (Green Line)
Path: Whitefield → ... → Majestic → ... → Silk Institute
Distance: X km | Time: Y minutes | Interchanges: 1
```

### Seat Allocation
```
Passenger: John Doe (Age: 65, Elderly)
Allocated Seat: 15 (Door proximity, Non-AC zone)
Visual seat map with allocated positions displayed
```

## Evaluation Metrics
- **Heap Performance**: O(log n) insertion, deletion, and priority update operations
- **Route Optimization**: Shortest distance and time calculations using efficient algorithms
- **Memory Efficiency**: HashMap-based indexing for O(1) element access in heap
- **Allocation Efficiency**: Priority-based seat assignment success rate
- **Health Safety**: Proper separation of infectious and susceptible passengers
- **User Experience**: Multi-format input handling and clear output presentation

## Future Enhancements
- Real-time metro schedule integration
- Mobile application interface
- Dynamic seat availability updates
- Metro card system integration
- Multi-language support
- Web-based user interface
- Integration with live metro APIs
## 📄 Published Paper

**Title:** Optimizing Urban Transit: Adaptive and Inclusive Seating Allocation Strategies

**Authors:** Kandibanda Lohith, Mudumala Varnika Narayani, Naga Ruthvika Durupudi, Nunnaguppala Rohit, Nandu C Nair

**Publication:** 2025 IEEE International Conference on Interdisciplinary Approaches in Technology and Management for Social Innovation (IATMSI)

**Conference Date:** 06-08 March 2025  
**Conference Location:** Gwalior, India  
**Publisher:** IEEE

**Abstract:** The evolution of public transportation systems demands innovative approaches to enhance passenger comfort and operational efficiency. Current seating arrangements often overlook the varied needs of passengers, leading to suboptimal experiences. This research introduces an adaptive seating allocation system that leverages advanced data structures, particularly priority queues, to dynamically assign seats based on criteria such as age, pregnancy status, and health conditions. This prioritization aims to ensure that vulnerable passengers, including the elderly and those with medical needs, are seated in optimal locations to maximize safety and comfort. The proposed system also incorporates secondary considerations, such as proximity to exits for quick disembarkation, improved ventilation for respiratory comfort, and minimizing exposure to potential health risks. Realtime sensor data and feedback mechanisms facilitate continuous adjustments to seating configurations, accommodating shifts in passenger demographics throughout the day. This adaptive strategy promotes crowd management and overall system efficiency while fostering a more inclusive travel experience. The integration of these adaptive seating solutions addresses common challenges in urban transit, contributing to higher passenger satisfaction and a more effective public transportation system. By prioritizing individual needs and safety, these enhancements represent a critical step toward a modern, user-centered approach to urban mobility.

**DOI:** [10.1109/IATMSI64286.2025.10984445](https://doi.org/10.1109/IATMSI64286.2025.10984445)

**IEEE Xplore:** [📖 Read Full Paper](https://ieeexplore.ieee.org/document/10984445)
## Team Members (Amrita School of Computing, Bengaluru)
*B.Tech CSE, Batch of 2022–2026*  
**Amrita School of Computing, Bengaluru**  
**Amrita Vishwa Vidyapeetham, India**

- **Naga Ruthvika Durupudi**
- **Kandibanda Lohith**
- **Mudumala Varnika Narayani**
- **Nunnaguppala Rohit**
---

## 🎓 Mentor

- **Dr. Nandu C Nair**  
  Associate Professor  
  Department of Computer Science and Engineering  
  Amrita School of Computing, Bengaluru  
  Amrita Vishwa Vidyapeetham, India

## 🙏 Acknowledgment

This project was developed as part of the academic curriculum for the **B.Tech CSE Batch of 2022–2026** under the mentorship of **Dr. Nandu C Nair**, Amrita School of Computing, Amrita Vishwa Vidyapeetham, Bengaluru campus.

---

> 📚 Developed as part of the academic curriculum at  
> **Amrita School of Computing, Bengaluru**  
> **Amrita Vishwa Vidyapeetham, India**


