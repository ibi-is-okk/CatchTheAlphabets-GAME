# **Catch the Alphabets Game** 🎮

Welcome to **Catch the Alphabets**, a simple assembly language game where you catch falling alphabets to score points while avoiding penalties to your lives!

---

## **Game Overview** 🕹️

The game is written entirely in **8086 Assembly Language** and runs in text mode using **BIOS interrupts** to manipulate the screen. Here's what happens:

- Alphabets fall randomly from the top of the screen.
- Use the **left** and **right arrow keys** to move the catcher (a blue box) horizontally.
- Catch the alphabets to gain points.
- Missing alphabets reduces your **lives**.
- If you lose all your lives, it's **Game Over!**

---

## **Features** ✨

- **Score Tracking:** Points are displayed in real time as you catch alphabets.
- **Dynamic Speed:** Alphabets fall at varying speeds for an exciting challenge.
- **Lives Display:** Heart symbols represent remaining lives.
- **Game Over Screen:** Displays your final score at the end.

---

## **How to Play** 🕹️

1. **Run the Game:**
   - Assemble the code using an assembler like **NASM** or **MASM**.
   - Load and run the `.COM` file in **DOSBox** or another x86 emulator.

2. **Controls:**
   - **Arrow Keys:** Move the catcher box left or right.
   - **Esc Key:** Exit the game.

3. **Objective:**
   - Catch as many alphabets as possible to maximize your score.
   - Avoid missing alphabets to keep your lives intact.

---

## **Code Breakdown** 📜

### **Main Components**

1. **`clrscr:`**
   - Clears the screen using video memory at `0xB800`.

2. **`score:`**
   - Updates and displays the current score in real time.

3. **`movalphabets:`**
   - Handles the movement of alphabets and detects collisions.

4. **`game:`**
   - Sets up the game's introductory messages and visuals.

5. **`decrementLife:`**
   - Updates the hearts when a life is lost.

6. **`GenRandom:`**
   - Generates random positions and characters for falling alphabets.

---

## **System Requirements** 🖥️

- **Operating System:** DOS or an x86 emulator (e.g., **DOSBox**).
- **Assembler:** Any assembler capable of producing `.COM` files (e.g., **NASM**, **MASM**).

---

## **How to Build and Run** 🚀

1. **Assemble the code:**
   ```bash
   nasm -f bin game.asm -o game.com
