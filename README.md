# 🏠 HouseQuest

A full-stack web application built using Java technologies that helps users find the **nearest and most affordable houses** using **Dijkstra’s shortest path algorithm**. The system intelligently ranks results based on **distance** and **price**, offering powerful search and filtering features.

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Architecture](#-architecture)
- [Features](#-features)
- [Algorithm Overview](#-algorithm-overview)
- [Technologies Used](#-technologies-used)
- [Usage](#-usage)
- [Contributing](#-contributing)
- [Screenshots](#-screenshots)

---

## 🎯 Overview

**HouseQuest** is a dynamic property discovery platform designed to help users find the **best possible house options** near their current location.  
It leverages **Dijkstra’s algorithm** to determine the shortest path to each available house, balancing both **distance** and **price preferences**.  
Users can easily filter results based on **minimum and maximum price ranges**, making home selection more efficient and data-driven.

---

## 🏗️ Architecture

### MVC Pattern Implementation

The app follows the **Model-View-Controller (MVC)** architectural pattern for clean separation of concerns and modular design.

#### Frontend (View)
- **JSP (Java Server Pages):** Dynamic content rendering  
- **HTML5:** Structural layout  
- **CSS3:** Styling and responsive UI  
- **JavaScript:** DOM manipulation and interactivity  

#### Controller
- **Java Servlets:** Handle requests, manage routes, and link the frontend with backend logic.  
- **Functionality:**
  - Receives user input for current location and price range
  - Triggers shortest path computation via helper classes
  - Returns ranked house results to the frontend  

#### Backend (Model)
- **Database:** MySQL Workbench (SQL)
  - Stores house data (ID, coordinates, price, availability)
  - Maintains graph relationships between locations  
- **Model Classes:** Represent graph nodes, edges, and house entities  
- **Server:** Apache Tomcat  

### Architecture Flow
1. User submits their current location and searches
2. Servlet forwards the request to the backend helper class.  
3. **Dijkstra’s algorithm** computes the shortest path from the source to each house node.  
4. Backend ranks and filters houses by distance and price.  
5. Results returned and rendered via JSP for a seamless user experience.  

---

## ✨ Features

### 🧭 Intelligent House Search
- Implements **Dijkstra’s algorithm** to calculate the shortest travel paths to each house.  
- Computes optimal distance considering multiple possible routes.  
- Returns results sorted by nearest distance.

### 💰 Price-Based Filtering
- Users can set **minimum** and **maximum** price filters.  
- Combines both **distance and affordability** to show best-fit results.  
- Automatically removes houses outside the selected budget range.

### 👤 User Interface
- Clean and intuitive layout built using JSP, CSS, and JS  
- Real-time updates when filters or parameters change  
- Dynamic display of search results with distance and price details  

### 🔒 Authentication & Data Management
- Secure user login and registration system  
- Stores search history and preferred locations  
- Validates user credentials against database entries  

---

## 🧮 Algorithm Overview

### Dijkstra’s Shortest Path
The algorithm identifies the shortest path from the user's current location to all available houses.  

**Implementation Steps:**
1. Represent city layout as a **weighted graph** (nodes = locations, edges = distances).  
2. Apply **Dijkstra’s algorithm** to calculate the minimum distance from the source node.  
3. Store and rank houses based on the 
---

## 🛠️ Technologies Used

### Backend
- **Java** — Core application logic  
- **Java Servlets** — Request handling and routing  
- **JSP (Java Server Pages)** — Server-side rendering  
- **MySQL** — Database management  
- **Apache Tomcat** — Deployment server  

### Frontend
- **HTML5** — Structure and semantics  
- **CSS3** — Styling and responsive layout  
- **JavaScript** — Interactive elements and input handling  

### Algorithm Layer
- **Dijkstra’s Algorithm** — Shortest path computation  
- **Graph Data Structures** — Node-edge relationships representing city map  

---

## 📱 Usage

1. **Register/Login** — Create a new user account or log in with existing credentials.  
2. **Enter Location** — Provide your current position as the starting node.  
3. **Set Price Filters** — Choose minimum and maximum house prices.  
4. **Find Houses** — View ranked results based on distance and price.  
5. **View Details** — Click on any house card for location, price, and route details.  

---

## 🤝 Contributing

Contributions are welcome!  
To contribute:
1. Fork the repository  
2. Create a new branch (`feature/your-feature-name`)  
3. Commit your changes  
4. Submit a pull request 🚀  

### Future Enhancements
- 🗺️ Integration with Google Maps API for real-time route visualization  
- 📊 Weighted scoring combining distance, price, and user rating  
- 📱 Responsive mobile app version  
- 🧠 AI-based house recommendation engine  

---

## 📸 Screenshots

| Search Page | Search Results |
|------------|-------------|
| ![Search](login.png) | ![Search Results](register.png) |

### Main Application Interface
| Price Filter | Price filter |
|-----------|--------------|
| ![Ordered by lowest price](dashboard.png) | ![Ordered by highest price](player.png) |

---

Developed with ❤️ by **Aishwarya Ravichandran**  
_Last Updated: November 2025_
shortest computed distance.  
4. Combine with price filter logic for optimal results.  


