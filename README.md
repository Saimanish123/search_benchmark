# Search Algorithm Benchmarking Tool

A comprehensive platform for running, comparing, and analyzing classical search algorithms. Built for DSE 3241 — Principles of Artificial Intelligence.

## 🚀 Features

* **Multiple Algorithms**: Includes implementations of Breadth-First Search (BFS), Depth-First Search (DFS), Uniform-Cost Search (UCS), Greedy Best-First Search (GBFS), and A* Search.
* **Environments**: Test algorithms on two distinct problem spaces:
  * **Weighted Graphs**: Configurable node counts and edge densities.
  * **Grid Mazes**: Customizable dimensions and wall densities.
* **Benchmarking Suite**: Compare multiple algorithms simultaneously to evaluate runtime, memory usage, path cost, and node expansions.
* **Heuristic Analysis**: Evaluate custom heuristics for admissibility and consistency.
* **Agent Strategy Selector**: An intelligent agent that recommends the optimal search strategy based on given constraints (speed, memory, optimality).
* **Visualization & Analytics**: Generate detailed charts comparing algorithm performance metrics.
* **Web Interface**: A sleek, user-friendly frontend built in HTML/JS interacting with a FastAPI backend.

## 🛠️ Tech Stack

* **Backend**: Python 3.x, FastAPI, Uvicorn
* **Data Processing & Analysis**: NumPy, Pandas, Matplotlib
* **Frontend**: Vanilla HTML / JS (interacting via REST API)

## ⚙️ Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Saimanish123/search_benchmark.git
   cd search_benchmark
   ```

2. **Create and activate a virtual environment (optional but recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```

3. **Install the dependencies:**
   ```bash
   pip install fastapi uvicorn numpy pandas matplotlib
   ```

4. **Run the backend server:**
   ```bash
   python api.py
   ```

5. **Open the Web Interface:**
   Navigate to `http://localhost:8000` in your web browser.

## 📖 API Endpoints

The backend provides several endpoints for running tasks programmatically. You can view the full interactive API documentation by navigating to `http://localhost:8000/docs` while the server is running.

Some key endpoints include:
* `POST /generate/graph` — Generate a random weighted graph
* `POST /generate/grid` — Generate a random grid maze
* `POST /solve` — Run a single algorithm on a generated problem
* `POST /benchmark` — Run all algorithms and compare results
* `POST /run/experiment` — Run heavy benchmarking suites and generate charts

## 📊 Project Structure

* `/api.py` - Main FastAPI backend application
* `/index.html` - Web user interface
* `/search_benchmark/algorithms/` - Implementations of the search algorithms
* `/search_benchmark/core/` - Problem definitions (Grids, Graphs) and Heuristics
* `/search_benchmark/analysis/` - Tools for heuristic analysis and chart generation
* `/search_benchmark/benchmarking/` - Runner and experiments framework
* `/search_benchmark/agent/` - AI Agent for strategy selection
* `/tests/` - Unit tests for algorithms and components
