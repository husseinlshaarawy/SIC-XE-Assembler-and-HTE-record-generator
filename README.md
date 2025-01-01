# SIC/XE Assembler and HTE Record Generator

This repository contains an assembler for the **SIC/XE architecture**, designed to convert assembly language programs into machine code. Additionally, it generates **HTE (Header, Text, End)** records for object programs, facilitating program execution on the SIC/XE machine.

## Features

- **Two-Pass Assembler**:
  - **Pass 1**: Constructs the symbol table, calculates memory addresses, and processes labels.
  - **Pass 2**: Generates machine code and object program records.
- **HTE Record Generation**:
  - **Header Record (H)**: Includes program name, starting address, and program length.
  - **Text Records (T)**: Contain the actual machine instructions and data.
  - **End Record (E)**: Marks the end of the object program and specifies the starting execution address.
- **Error Detection**: Identifies and reports common issues, such as:
  - Invalid opcodes.
  - Undefined symbols.
  - Addressing mode mismatches.
- **Modular Design**: Clear separation between assembly, symbol management, and record generation for ease of maintenance.

## How to Use

1. Clone the repository:
   git clone https://github.com/your-username/SIC-XE-Assembler-and-HTE-record-generator.git
   cd SIC-XE-Assembler-and-HTE-record-generator
Compile the source code:

[Insert specific command here, e.g., gcc assembler.c -o assembler]
Provide a SIC/XE assembly program as input.

Run the assembler to generate:

Symbol Table: A list of program symbols and their memory locations.
Object Program: Machine code instructions.
HTE Records: H, T, and E records for object programs.
Verify the output using a SIC/XE simulator or debugging tool.

File Structure
├── main.java/          # Source code for the assembler
├── SICXE.txt/     # Sample SIC/XE assembly programs
├── SICXE_Final.txt/       # Generated object programs and HTE records
└── README.md     # Project overview and instructions
Examples
Input: Sample Assembly Code
asm
Copy code
COPY    START   1000
FIRST   LDA     NUM
        ADD     FIVE
        STA     RESULT
NUM     WORD    3
FIVE    WORD    5
RESULT  RESW    1
        END     FIRST


Output: HTE Records
H^COPY^001000^00000F
T^001000^0C^001003^001005^001009
E^001000

License
This project is licensed under the MIT License.

Feel free to reach out with suggestions, issues, or questions. Happy coding!


Let me know if you'd like further customization or additional details!
