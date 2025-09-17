# AI Car Racing Simulation

This project is an interactive AI car racing simulation built with Python and Pyglet. It demonstrates how neural networks and genetic algorithms can be used to evolve self-driving cars that learn to navigate a racetrack.

---

## 🚗 Project Overview

- **AI Cars**: Each car is controlled by a neural network ("brain") that receives input from virtual sensors (radars) and outputs steering and acceleration commands.
- **Genetic Algorithm**: The best-performing cars are selected, crossed over, and mutated to create new generations that improve over time.
- **Visualization**: The simulation is visualized using Pyglet, showing the racetrack, cars, checkpoints, and neural network activity.

---

## 🧠 How It Works

1. **Simulation**: Cars start with random neural networks and attempt to drive around the track.
2. **Sensing**: Each car uses 5 radars to sense the distance to the track edge.
3. **Decision Making**: The neural network processes radar inputs and outputs acceleration and steering.
4. **Evolution**: After each round, the best cars are selected, and their neural networks are evolved to form the next generation.
5. **Learning**: Over many generations, cars learn to drive better and reach more checkpoints.

---

## 📂 Project Structure

- `canvas.py`: Main simulation and rendering engine. Handles drawing, simulation loop, and user input.
- `car.py`: Car and radar logic. Each car has sensors and a neural network.
- `network.py`: Neural network implementation and serialization for evolution.
- `evolution.py`: Genetic algorithm for evolving networks (selection, crossover, mutation).
- `racetrack.py`: Track loading, checkpoint management, and road detection.
- `hud.py`: Heads-up display for stats and neural activity.
- `storage.py`: Save/load best neural networks to/from disk.
- `training.py`: Main training script. Runs the evolution process.
- `testdrive.py`: Runs the best saved networks for demonstration.
- `images/`: Track and car images.
- `brain.json`: Saved best neural networks.

---

## 🏁 Getting Started


### Prerequisites

- Python 3.10+
- [Pyglet](https://pyglet.readthedocs.io/en/latest/) (`pip install pyglet`)

**No external machine learning libraries are used!**

This project is implemented using only pure Python and the built-in `math` module. There is no use of numpy, pytorch, tensorflow, or any other ML/AI libraries. All neural network and genetic algorithm logic is written from scratch 

### Running the Simulation

1. **Train the AI Cars**  
   Run the training script to evolve the car controllers:
   ```bash
   python training.py
   ```

2. **Test the Best Cars**  
   After training, watch the best cars drive using:
   ```bash
   python testdrive.py
   ```

### Controls

- Press `ESC` to stop the simulation.

---

## 📝 Code Details

### `canvas.py`
Handles the main simulation window, drawing the track, cars, checkpoints, and HUD. Manages the simulation loop and user input.

### `car.py`
Defines the `Car` class, which uses 5 radars to sense the environment. The car's neural network receives these inputs and outputs acceleration and steering.

### `network.py`
Implements a simple feedforward neural network. Supports serialization/deserialization for use with the genetic algorithm.

### `evolution.py`
Implements the genetic algorithm: selects the best cars, performs crossover and mutation, and generates new networks for the next generation.

### `racetrack.py`
Loads the racetrack image, overlay, and checkpoints. Provides a method to check if a car is on the road.

### `hud.py`
Draws the heads-up display, showing simulation stats and a visualization of the neural network's activity.

### `storage.py`
Handles saving and loading the best neural network weights (chromosomes) to/from a JSON file.

### `training.py`
Main script for training the AI cars. Runs multiple generations, evolving the networks each time, and prints stats after each round.

### `testdrive.py`
Loads the best saved networks and lets you watch them drive (no evolution).

---

## 📚 Example

- Cars start with random behavior and quickly crash.
- Over generations, some cars learn to follow the track and reach more checkpoints.
- The best-performing neural networks are saved and can be replayed.

---

## 🤝 Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.

---

## 📄 License

MIT License

---

Feel free to add screenshots, GIFs, or further instructions as needed!# 🚗 AI Car Racing Simulation  

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


