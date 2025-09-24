# Under the Hood: Embedded System Memory & Assembly Lab

This repository presents my work on embedded systems fundamentals with a focus on memory organization, C-to-assembly translation, and dynamic memory management.
The project was originally developed as a lab exercise and has been adapted into a GitHub research-style portfolio to showcase low-level programming and hardware/software co-design skills.

---

## Repository Structure

```
under-the-hood-embedded-lab/
├── README.md
├── LICENSE
├── .gitignore
├── report/
│   └── UnderTheHood_LabExercise.pdf   # Anonymized version of the report
├── code/
│   ├── main.c                         # Main program (counter, delay functions)
│   └── delay.c                        # Delay routine in C
└── figures/
    ├── memory_map.png                 # SRAM/GPR/SFR memory layout diagram
    └── instruction_summary.png        # Example PIC assembly instructions
```

---

## Project Overview

This project explores the internal architecture of a PIC18F46K22 microcontroller and demonstrates how C code translates into machine-level instructions.
Key learning areas:

- Flash, SRAM, and EEPROM structure
- General Purpose Registers (GPR) vs Special Function Registers (SFR)
- Mapping of C functions to assembly/hex instructions
- Understanding indirect addressing and arrays in memory
- Using dynamic memory allocation (`malloc`) in embedded C

---

## Key Features

1. **Memory Analysis**
   - Organization of Flash, SRAM, and EEPROM
   - Role of GPR and SFR registers
   - Memory addressing and instruction cycles

2. **C-to-Assembly Translation**
   - Counter program in C → assembly instructions
   - Delay function breakdown
   - Instruction set summary

3. **Dynamic Memory Management**
   - Use of `malloc()` in embedded C
   - Dynamic allocation tables
   - Impact on RAM usage

4. **Practical Programming**
   - Arrays initialization
   - Indirect addressing
   - Debugging embedded code

---

## Example Code Snippet

```c
#include <xc.h>
#define _XTAL_FREQ 4000000

void delay_ms(unsigned int ms) {
    while(ms--) {
        __delay_ms(1);
    }
}

void main(void) {
    int counter = 0;
    while(1) {
        counter++;
        delay_ms(1000); // Increment every second
    }
}
```

---

## How to Use

1. Open `report/UnderTheHood_LabExercise.pdf` for full documentation (anonymized version).
2. Explore the `code/` folder for C implementations of the counter and delay routines.
3. Review `figures/` for visual diagrams of memory mapping and instruction sets.

---

## Notes

- Original work was prepared as a lab exercise.
- Sensitive information (student name/ID, academic integrity declaration) should be anonymized before publishing.
- This repository is intended as a portfolio project to demonstrate low-level programming and embedded system knowledge.

---

## Author

**Jinyan Yang** — MSc in Renewable Energy Systems
