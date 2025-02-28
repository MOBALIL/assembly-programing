# Running Assembly Programs with NASM on Linux

# Requirements
Ensure you are using a Linux-based operating system to execute these programs.

## Compiling and Running with NASM

### 1. Greetings Program

1. Save your assembly source code in a file, for example, `greet.asm`.
2. Assemble the file using NASM:
   ```bash
   nasm -f elf32 greet.asm -o greet.o
   ```
3. Link the object file to create an executable:
   ```bash
   ld -m elf_i386 greet.o -o greet
   ```
4. Execute the program:
   ```bash
   ./greet
   ```
   **Expected Output:**
   ```
   Greetings, World!
   ```

### 2. Segmented Greetings Program

1. Save your assembly code in `greet_segments.asm`.
2. Assemble and link the program:
   ```bash
   nasm -f elf32 greet_segments.asm -o greet_segments.o
   ld -m elf_i386 greet_segments.o -o greet_segments
   ```
3. Run the executable:
   ```bash
   ./greet_segments
   ```
   **Expected Output:**
   ```
   Greetings from .data!
   Hello there from .data!
   Greetings from .text!
   ```

