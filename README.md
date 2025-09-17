
# AI Car Racing Simulation

An AI-powered car racing simulation built with **Python** and **Pyglet**. This project demonstrates how simple neural networks and genetic algorithms can evolve self-driving cars to navigate a racetrack—using only pure Python and the built-in `math` module (no numpy, pytorch, tensorflow, or other ML libraries).

---

## 🚗 Project Overview

- **AI Cars**: Each car is controlled by a neural network ("brain") that receives input from virtual sensors (radars) and outputs steering and acceleration commands.
- **Genetic Algorithm**: The best-performing cars are selected, crossed over, and mutated to create new generations that improve over time.
- **Progressive Learning**: Cars evolve from random driving to skilled track navigation.
- **Visualization**: The simulation is visualized using Pyglet, showing the racetrack, cars, checkpoints, and neural network activity.
- **Replay System**: Best-performing models can be saved and replayed later.

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



## Detailed Project Explanation

This project is a self-driving car simulation and evolution environment, built entirely in Python using the Pyglet library for graphics. The goal is to evolve cars that can drive themselves around a racetrack using only simple neural networks and a genetic algorithm. Everything is implemented from scratch using pure Python and the built-in `math` module—no numpy, pytorch, tensorflow, or other machine learning libraries.

### How the Simulation Works

1. **Environment & Visualization**: The racetrack is loaded from images and JSON files. Cars are visualized as sprites and move around the track. Each car is equipped with 5 virtual radars (sensors) that measure the distance to the track edge in different directions.

2. **Neural Network Brains**: Each car has a small feedforward neural network (see `network.py`). The network takes the 5 radar distances as input and outputs two values: acceleration and steering. The network is implemented from scratch, with all math done manually.

3. **Genetic Algorithm**: At the start, all cars have random neural network weights. After each simulation round, cars are ranked by how many checkpoints they passed and how far they stayed from the track edge. The best-performing cars are selected. New generations are created by crossing over and mutating the weights of the best cars. Over many generations, the population of cars gets better at driving.

4. **Heads-Up Display (HUD)**: The simulation is rendered in real time using Pyglet. You can see the cars, the track, checkpoints, and a HUD showing stats and neural network activity.



## Demo Screenshot

Below is a screenshot of the simulation in action:

![AI Car Simulation Screenshot](images/Screenshot%202025-09-16%20at%209.24.48%E2%80%AFPM.png)

---

## 📚 Example Workflow

1. Cars start with random behavior and quickly crash.
2. Over generations, some cars learn to follow the track and reach more checkpoints.
3. The best-performing neural networks are saved and can be replayed.

---

## 🤝 Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.

---





