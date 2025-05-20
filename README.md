Mini Operating System Simulation
Overview
A C++-based mini operating system simulating process management, multi-threading, priority scheduling, context switching, and shared memory. It supports 15 predefined tasks (e.g., Calculator, Tic Tac Toe) with user and kernel modes for task execution and management.
Features

POSIX threads for concurrent task execution.
Priority-based scheduling and context switching.
Shared memory for RAM management.
User mode: Menu-driven task execution.
Kernel mode: Task addition/deletion (password: 1122).
Task manager displaying active tasks.
Queues for task management.

Prerequisites

OS: Linux (requires gnome-terminal).
Compiler: GCC (C++11 or later).
Libraries: <pthread.h>, <sys/shm.h>, standard C++ libraries.
Dependencies: Task-specific .cpp files (e.g., calculator.cpp, tictactoe.cpp).

Installation

Place task-specific .cpp files in the same directory.
Compile the main program:g++ main.cpp -o os_sim -pthread


Compile each task file, e.g.:g++ calculator.cpp -o calculator



How to Run
Run with three command-line arguments: RAM (MB), CPU cores, disk size (MB):
./os_sim 100 4 500


Example: Allocates 100 MB RAM, 4 cores, 500 MB disk.

Usage

Startup: Shows loading screen, launches calender and time tasks in gnome-terminal.
Login:
User Mode (1): Choose tasks (1–15) or shutdown (16).
Kernel Mode (2): Enter password 1122 to add/delete tasks or shutdown (3).


Tasks execute in separate terminals; RAM usage is tracked.
Task manager displays running tasks periodically.

Task List

Calculator (10 MB, Priority 1)
Tic Tac Toe (30 MB, Priority 2)
Binary Search (40 MB, Priority 4)
Banking System (2 MB, Priority 3)
Guessing Game (2 MB, Priority 3)
Message Box (30 MB, Priority 6)
Create File (6 MB, Priority 8)
Delete File (3 MB, Priority 7)
Calendar (10 MB, Priority 9)
Time (30 MB, Priority 10)
Find Factorial (11 MB, Priority 11)
String Length (11 MB, Priority 12)
Find Prime (20 MB, Priority 9)
Hangman (15 MB, Priority 19)
Stop Watch (11 MB, Priority 15)

Notes

Task-specific .cpp files must be implemented.
Linux-specific due to gnome-terminal usage.
Limited error handling for missing files or compilation issues.

Troubleshooting

Compilation Errors: Ensure task .cpp files exist.
Terminal Issues: Install gnome-terminal (sudo apt-get install gnome-terminal).
Shared Memory: Verify shared memory permissions.


Author
Muhammad Hamza Saleem
