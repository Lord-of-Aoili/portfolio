# 🕹️ Pac-Man (JavaFX Implementation)

![Pac-Man Screenshot](../assets/pacman.png)

## 🚀 Overview
This is a **JavaFX-based Pac-Man game**, implemented as part of an **Object-Oriented Design** course. The game extends a provided scaffold by adding:
- **New Ghost AI Behaviors**
- **Power Pellet Mechanics**
- **Frightened Mode for Ghosts**
- **Enhanced Gameplay Dynamics Using Design Patterns**

This project emphasizes **OOP principles, software design patterns, and clean architecture**.

🔗 **Live Demo:** *(if applicable)*  
📜 **Source Code:** [GitHub Repository](https://github.com/Lord-of-Aoili/pacman-javafx)

---

## 🎮 Features

### **👻 Additional Ghost Types**
Implemented **four unique ghost behaviors**:
| Ghost | Chase Mode Target | Scatter Mode Target |
|--------|-----------------|------------------|
| **Shadow (Blinky)** | Targets Pac-Man’s position | Top-right corner |
| **Speedy (Pinky)** | Four tiles ahead of Pac-Man | Top-left corner |
| **Bashful (Inky)** | Uses a relative offset from Blinky | Bottom-right corner |
| **Pokey (Clyde)** | Targets Pac-Man if far, else bottom-left | Bottom-left corner |

Each ghost uses **AI-driven movement logic** to dynamically respond to Pac-Man’s position.

---

### **🟠 Power Pellet Mechanics**
- When Pac-Man eats a **Power Pellet**, ghosts enter **FRIGHTENED mode**.
- Ghosts become **slower** and move **randomly**.
- If Pac-Man eats a frightened ghost, it **respawns** after a delay.

| Ghost Eaten | Points Awarded |
|------------|--------------|
| 1st Ghost  | 200 Points |
| 2nd Ghost  | 400 Points |
| 3rd Ghost  | 800 Points |
| 4th Ghost  | 1600 Points |

---

## 🔧 Installation & Setup

### **1️⃣ Clone the Repository**
```sh
git clone https://github.com/Lord-of-Aoili/pacman-javafx
cd pacman-game
```

### **2️⃣ Build & Run Using Gradle**
```sh
gradle clean build run
```
💡 Ensure you have **JDK 17** and **Gradle 7.4.2** installed.

### **3️⃣ Open the Game**
The game should launch in a JavaFX window.

---

## 🏗️ Software Design
### **🔹 Applied Design Patterns**
This implementation follows **three major design patterns**:
1. **Strategy Pattern** → Ghost behaviors (Chase, Scatter, Frightened)
2. **State Pattern** → Ghost state transitions
3. **Factory Pattern** → Creating game entities dynamically

A UML diagram illustrating these relationships is available in the repository.

---

## 📜 Project Structure
```
pacman-game/
│── src/
│   ├── main/
│   │   ├── java/
│   │   │   ├── pacman/        # Core game logic
│   │   │   ├── pacman/ghosts/  # Ghost AI
│   │   │   ├── pacman/ui/      # JavaFX UI components
│   │   │   ├── pacman/items/   # Pellets & power-ups
│   ├── resources/
│   │   ├── config.json         # Game settings
│   │   ├── map.txt             # Game map
│   │   ├── new-map.txt         # Updated map
│   │   ├── sprites/            # Game graphics
│── build.gradle
│── README.md
```

---

## 🖼️ Screenshots
![Pac-Man Gameplay](../assets/pacman.png)

---

## 📜 License
This project is licensed under the MIT License.

---

## 🔗 Related Links
- 🔗 [GitHub Repository](https://github.com/Lord-of-Aoili/pacman-javafx)

