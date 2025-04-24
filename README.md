# Procedures
# 👋 8086 Assembly: Hello World with Procedures

This is a basic **8086 Assembly Language** program that demonstrates:
- **Modular programming** using `PROC` procedures
- Printing messages using **INT 21h**
- Outputting text across **multiple lines**

---

## 📜 What It Does

- Prints: Hello World
- Separates the two messages using a newline
- Uses separate **procedures** for each task:
- `printstring1` → prints `"Hello"`
- `new` → adds a new line
- `printstring2` → prints `"World"`

---

---

## 💻 How to Run

### 🛠️ Using EMU8086

1. Paste the code into EMU8086
2. Compile and Run the program

## Output
![image](https://github.com/user-attachments/assets/673a77a0-d98a-4406-9d69-147da3253f6f)

# 🔢 8086 Assembly: Sum of Three Numbers (with Procedures)

This 8086 Assembly Language program takes **three single-digit numbers** as input from the user, calculates their **sum**, and prints the result using **modular procedures**.

---

## 🎯 Features

- Prompts the user for:
  - First number
  - Second number
  - Third number
- Calculates the sum of all three
- Displays the sum
- Uses separate procedures:
  - `Input` → for input
  - `Sum` → for computation
  - `Output` → for displaying result

---

## 🧩 How It Works

### Input Phase:
- Uses `INT 21h / AH=1` to take keyboard input
- Converts ASCII to integer by subtracting 48
- Stores inputs in registers `BL`, `BH`, and `CL`

### Sum Phase:
- Adds `BL + BH + CL`
- Result stored in `BL`

### Output Phase:
- Prints: `Sum of three numbers: X`
- Converts result back to ASCII using `+48`
- Uses `INT 21h / AH=2` for single-character output

---

## 💬 Sample Output

![image](https://github.com/user-attachments/assets/067b64c5-baba-4880-87b5-40682660add7)

# 🧮 8086 Assembly: String Length Counter

This 8086 Assembly Language program prompts the user to **enter a string** and then displays its **length** using DOS interrupts and basic string handling logic.

---

## 🧠 What It Does

- Prompts user with: `Enter String:`
- Reads input string (max 25 characters)
- Calculates string length
- Displays: `Length is: X`

---

## 📂 Program Structure

The program is modular and uses the following procedures:

- `Input` → to take user input string
- `Length` → to calculate and display the string length

---

## 🔍 Code Breakdown

### `Input` Procedure
- Uses `INT 21h / AH=1` to read characters one by one
- Ends when **Enter key (Carriage Return, ASCII 13)** is pressed
- Stores characters in `st[]` and counts using `SI`

### `Length` Procedure
- Moves the count in `SI` to a variable `len`
- Uses division to convert integer length to ASCII for display
- Prints the result using `INT 21h / AH=2`

---

## 💬 Sample Output

![image](https://github.com/user-attachments/assets/4c52b445-bbdc-4978-ab5d-93213384a730)


