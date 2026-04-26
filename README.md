## Overview
The project is a simple GUI editor written in C using a custom windowing system. It supports saving and loading files, text editing, and basic file operations.

## Features
- Basic text editing
- File opening, saving, and creating
- Custom windowing system for rendering

## Project Structure
```
GuiEditor/
├── build/              
├── bin/                
├── libs/               
├── lib/                
├── code/               
├── data/               
├── assets/             
├── src/                
│   ├── Main.c          # Entry point
│   └── *.h             # Standalone Header-based C-files, without *.c files that implement it
├── Makefile.linux      # Linux Build configuration
├── Makefile.windows    # Windows Build configuration
├── Makefile.wine       # Wine Build configuration for cross-compiling to Windows on Linux
└── README.md           # This file
├── LICENSE
└── .gitignore
```

### Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools

## Build & Run
The project uses four different makefiles for building on different platforms. Here’s how to build and run it:

### Linux Build
```bash
cd GuiEditor
make -f Makefile.linux all
make -f Makefile.linux exe  # Run the application
```

### Windows Build
```bash
cd GuiEditor
make -f Makefile.windows all
make -f Makefile.windows exe  # Run the application
```

### Wine Build (Cross-compiling to Windows on Linux)
```bash
cd GuiEditor
make -f Makefile.wine all
make -f Makefile.wine exe  # Run the application using Wine
```

### WebAssembly Build
```bash
cd GuiEditor
make -f Makefile.web all
make -f Makefile.web exe  # Serve the application via emrun (requires Emscripten)
```

# Build Steps
- Navigate to the project directory.
- Use `make -f Makefile.(os) all` for building.
- For a clean build, use `make -f Makefile.(os) clean` and then rebuild with `all`.

This setup allows you to compile and run the GUI editor on Linux, Windows, and even create WebAssembly for web-based execution.