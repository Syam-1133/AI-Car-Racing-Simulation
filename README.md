# 🚗 AI Car Racing Simulation  

An **AI-powered car racing simulation** built with **Python** and **Pyglet**.  
This project demonstrates how **neural networks** and **genetic algorithms** can work together to evolve self-driving cars that learn to navigate a racetrack over time.  

---

## 📖 Table of Contents  
1. [Features](#-features)  
2. [How It Works](#-how-it-works)  
3. [Project Structure](#-project-structure)  
4. [Getting Started](#-getting-started)  
   - [Prerequisites](#-prerequisites)  
   - [Installation](#-installation)  
   - [Running the Simulation](#-running-the-simulation)  
   - [Controls](#-controls)  
5. [Screenshots / Demo](#-screenshots--demo)  
6. [Code Highlights](#-code-highlights)  
7. [Example Workflow](#-example-workflow)  
8. [Future Improvements](#-future-improvements)  
9. [Contributing](#-contributing)  
10. [License](#-license)  

---

## 🌟 Features  
- **AI Cars**: Each car is controlled by a lightweight **feedforward neural network** ("brain").  
- **Virtual Sensors**: Cars use **5 radars** to sense distances to the track edges.  
- **Genetic Algorithm**:  
  - Selection → Best cars are chosen.  
  - Crossover → Neural networks are combined.  
  - Mutation → Random tweaks are introduced.  
- **Progressive Learning**: Cars evolve from random driving to skilled track navigation.  
- **Visualization**: Real-time rendering of cars, track, checkpoints, and neural activity.  
- **Replay System**: Best-performing models can be saved and replayed later.  

---

## 🧠 How It Works  
1. **Initialization**: Cars begin with randomly generated neural networks.  
2. **Sensing**: Each car has **5 radars** that measure distances to nearby walls.  
3. **Decision Making**:  
   - Inputs (radar distances) → Neural Network → Outputs (steering & acceleration).  
4. **Fitness Evaluation**: Cars earn a score based on distance traveled and checkpoints crossed.  
5. **Evolution Process**:  
   - The top cars are kept.  
   - Crossover and mutation create new offspring.  
   - Weak performers are replaced.  
6. **Learning**: Over generations, cars gradually learn how to follow the track.  

---

## 📂 Project Structure  
