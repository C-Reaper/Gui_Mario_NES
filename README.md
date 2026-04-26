# Project README

## Overview
The project is a C application that implements basic game mechanics for an NES-style game. It uses a custom entity system where each entity has its own behavior, such as movement and collision detection.

## Features
- Entity management
- Basic physics (gravity, acceleration)
- Collision detection
- Figure rendering (sprite-based entities)

## Project Structure

### Prerequisites
- C/C++ Compiler and Debugger (GCC)
- Make utility
- Standard development tools
- Libraries needed for the project (X11, ALSA)

## Build & Run

### Linux
To build on Linux, run:
```sh
cd <Project>
make -f Makefile.linux all
```

### Windows
To build on Windows, run:
```sh
cd <Project>
make -f Makefile.windows all
```

### Wine (Linux for Windows)
For cross-compiling to Windows using Wine on Linux, run:
```sh
cd <Project>
make -f Makefile.wine all
```

### WebAssembly
To build and serve the project as a web application, run:
```sh
cd <Project>
make -f Makefile.web all
make -f Makefile.web exe
```
Access the application in your web browser at `http://localhost:8080`.

---

# Project Organization

## Directory Structure
```
<Project>/
├── build/              # .exe files produced by Main.c
├── src/                # source code
│   ├── Main.c          # Entry point
│   └── *.h             # standalone Header-based C-files, without *.c files that implement it
├── Makefile.linux      # Linux Build configuration
├── Makefile.windows    # Windows Build configuration
├── Makefile.wine       # Wine Build configuration
├── Makefile.web        # Emscripten Build configuration
└── README.md           # This file
```

# Build Steps

## General Build Process
1. Navigate to the project directory.
2. Run `make -f Makefile.<os> all` to build the project for your specified operating system.

## Clean and Rebuild
To clean and rebuild the project:
```sh
make -f Makefile.<os> clean
make -f Makefile.<os> all
```

## Build Options
- `make -f Makefile.<os> all`: Builds the output.
- `make -f Makefile.<os> do`: Builds and executes the application.
- `make -f Makefile.<os> clean`: Removes build artifacts.

# Execute
To execute the built application, use:
```sh
make -f Makefile.<os> exe
```
Replace `<os>` with the appropriate target (linux, windows, wine, web).