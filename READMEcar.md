# 🚗 Car Control Console Program (Python)

## 📌 Description

This project is a **simple interactive console program written in Python** that simulates starting and stopping a car using text commands.

The program runs in a loop, accepts user input, and manages the **state of the car** (`start` / `stop`) while preventing redundant or illogical commands.

This project is designed for **learning purposes**, focusing on control flow, state management, and user interaction in Python.

---

## 🎯 Features

- Interactive command-line interface
- Supports the following commands:
  - `start` – starts the car
  - `stop` – stops the car
  - `help` – displays available commands
  - `quit` – exits the program
- Prevents repeating the same action unnecessarily
- Displays different messages when commands are repeated
- Tracks how many times `start` or `stop` is entered consecutively

---

## 🧠 Program Logic

The program uses:
- a `while True` loop for continuous execution
- dictionaries to manage:
  - the **current state** of the car
  - the **number of repeated commands**
- conditional statements (`if / elif / else`) to control behavior
- user input via `input()`

### State management example:
- If the car is already started and the user types `start` again, the program responds accordingly.
- The same logic applies to the `stop` command.

---

## ▶️ How to Run

1. Make sure you have **Python 3.x** installed.
2. Save the script as `car_control.py`
3. Run the program:

```bash
python car_control.py
