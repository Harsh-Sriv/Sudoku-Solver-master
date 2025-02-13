# Sudoku Solver 🧩

## Overview
A fast and efficient Sudoku solver implemented in C++ that uses backtracking algorithm to solve any valid Sudoku puzzle. The program can solve even the most challenging puzzles within milliseconds.

## Features
### Core Functionality
- **Fast Solving Algorithm** ⚡
  - Implements optimized backtracking algorithm
  - Solves most puzzles in under 1ms
  - Handles multiple puzzle difficulties

### Input/Output
- **Flexible Input Methods**
  - File input (.txt format)
  - Command-line input
  - Hard-coded puzzles
- **Clear Output Format**
  - Formatted grid display
  - Step-by-step solution visualization (optional)
  - Solving time statistics

## Requirements
- C++ compiler (GCC/G++ 5.0 or higher)
- CMake (version 3.10 or higher)
- Make

## Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/sudoku-solver.git
```

2. Navigate to project directory
```bash
cd sudoku-solver
```

3. Build the project
```bash
mkdir build
cd build
cmake ..
make
```

## Usage

### Command Line Input
```bash
./sudoku_solver
```
Then enter your Sudoku puzzle row by row, using 0 or . for empty cells:
```
5 3 0 0 7 0 0 0 0
6 0 0 1 9 5 0 0 0
0 9 8 0 0 0 0 6 0
...
```

### File Input
```bash
./sudoku_solver -f path/to/puzzle.txt
```

### Example Input File Format
```
5 3 0 0 7 0 0 0 0
6 0 0 1 9 5 0 0 0
0 9 8 0 0 0 0 6 0
8 0 0 0 6 0 0 0 3
4 0 0 8 0 3 0 0 1
7 0 0 0 2 0 0 0 6
0 6 0 0 0 0 2 8 0
0 0 0 4 1 9 0 0 5
0 0 0 0 8 0 0 7 9
```

## How It Works

### Algorithm
The solver uses a backtracking algorithm with the following optimizations:
1. Forward checking
2. Minimum remaining values heuristic
3. Constraint propagation

### Time Complexity
- Worst case: O(9^(n*n))
- Average case: Much faster due to optimizations

## Project Structure
```
sudoku-solver/
├── src/
│   ├── main.cpp
│   ├── solver.cpp
│   ├── solver.h
│   └── utils.h
├── tests/
│   ├── test_solver.cpp
│   └── puzzles/
├── examples/
│   └── sample_puzzles/
├── CMakeLists.txt
└── README.md
```

## Testing
Run the test suite:
```bash
cd build
./run_tests
```

## Contributing
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Performance Benchmarks
| Puzzle Difficulty | Average Solving Time |
|------------------|---------------------|
| Easy             | <1ms               |
| Medium           | ~2ms               |
| Hard             | ~5ms               |
| Expert           | ~10ms              |

## Future Improvements
- GUI implementation
- Puzzle generator
- Multiple solving algorithms
- Parallel processing for multiple puzzles

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author
Your Name ([@yourgithub](https://github.com/yourusername))

## Acknowledgments
- Donald E. Knuth for the Algorithm X concept
- Peter Norvig for his constraint propagation insights
