# Hillel Java Pro: Example in C

## Project structure
```sh
.
├── README.md
├── main.c          # main file / entry point
└── math            
    ├── math.c      # math lib implementation file
    └── math.h      # math lib header file
```

## How to build
- Compile math lib sources using GNU C compiler (GCC)
```sh
    cd math
    gcc -c math.c -Imath -o math.o
```
- Compile main file
```sh
    cd ..
    gcc -c main.c -Imath -o main.o
```
- Link main and math object code files
```sh
    gcc main.o math/math.o -o app
```

## How to run
- Execute binary
```sh
    ./app
```