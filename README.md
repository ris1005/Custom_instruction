# Custom_instruction
# 🧮 Custom Instruction Parser using Flex & Bison

This project implements a simple compiler front-end using **Flex** and **Bison** that parses a specific arithmetic expression and emits a custom instruction format. It's a minimal demonstration of how compiler tools can process and lower high-level code to a custom intermediate representation.

## 📄 Description

The parser is designed to recognize arithmetic expressions of the exact form:


## 🔍 Features

- ✅ Recognizes a fixed arithmetic pattern with parentheses and basic operators.
- ✅ Generates a meaningful intermediate instruction string.
- ✅ Uses typed symbols in Bison for safe and clear value handling.
- ✅ Demonstrates basic usage of Flex for tokenizing and Bison for parsing.
- ✅ Error handling for unexpected input structure.


## 📦 Technologies Used

- **Flex** – Lexical analyzer to tokenize source code.
- **Bison** – Parser generator to process grammar and generate code.
- **C** – Used as the host language for integration and output.

## 📥 Example Input
result = (a + b) * (c - d);
📤 Example Output 
Custom instruction: maddsub result, a, b, c, d
---
---
Github link: https://github.com/ris1005/Custom_instruction
---

⚙️ Build and Run Instructions
1. Save the Files
*  instgen.y (Bison file)
*  exprscan.l (Flex file)

4. Compile the Parser
5. Use the following commands in your terminal:
* bison -d instgen.y         # Generates parser.tab.c and parser.tab.h
* flex exprscan.l              # Generates lex.yy.c
* gcc -o parser instgen.tab.c lex.yy.c -lfl
  
6. Run the Parser
* ./parser
* Enter expression:result = (a + b) * (c - d);
You will see output:
Custom instruction: maddsub result, a, b, c, d




