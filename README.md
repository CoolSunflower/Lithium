# Lithium: A Hobby Programming Language

This repository contains the source code of the compiler (written in C) and grammar of Lithium: A Lightweight and Explosive Hobby Programming Language.

## Execution Steps:
Build the compiler:
```bash
cmake -S . -B build
cmake --build build
```

Make the script executable:
```bash
chmod +x lithium
```

Run the compiler with a .lit file:
```bash
./lithium test.lit
```