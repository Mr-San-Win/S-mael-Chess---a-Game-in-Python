---

# **Sam@el’s Chess — A Python & Tkinter Chess Application**

**Sam@el’s Chess** is a fully-functional chess application developed in **Python** using **Tkinter** and implemented entirely within a **single code file**.
The project demonstrates clean **Object-Oriented Programming (OOP)** design, complete **chess rule implementation**, user-friendly **graphical interfaces**, and basic **AI opponents**.

The system is designed for both academic assessment and practical gameplay, and includes an integrated **Learn Chess** module for beginners.

---

## **1. Overview**

This application provides a structured and interactive chess experience featuring:

* Two game modes (PvP and Human vs AI)
* A multi-page Tkinter GUI
* Complete enforcement of chess rules
* A modular OOP logic layer decoupled from the UI
* Move history, captured pieces tracking, and time controls
* Educational resources for new players

The project complies with formal software development requirements and demonstrates the application of OOP concepts within a single-file architecture.

---

## **2. Key Features**

### **Gameplay**

* **Player vs Player (Local)**
* **Human vs AI**

  * Club-Level AI (random but legal)
  * Strong AI (evaluation-based decision making)
* Highlighted legal moves
* Move history window
* Captured piece display
* Time control options (No limit, 5/10/30 minutes)

### **Chess Rules (All Implemented)**

* Legal movement validation
* **Castling** (full rule compliance)
* **En Passant**
* **Pawn Promotion**
* Check, checkmate, stalemate detection
* Illegal move prevention
* King-safety verification

### **User Interface (Tkinter)**

* Multi-frame navigation
* Clean dark-mode inspired theme
* Responsive board rendering
* Click-based piece selection
* “Back to Menu” navigation
* Integrated instructional page (“Learn Chess”)
* Scrollable content sections

---

## **3. Object-Oriented Architecture**

The project meets academic OOP requirements through a clean and expressive design:

### **3.1 Composition**

The central class `ChessGame` **owns**:

* An 8×8 board of `Piece` objects
* Game state attributes
* Captured piece lists
* Move history
* Castling/en-passant rights

This demonstrates **whole–part relationships** within the system.

### **3.2 Inheritance**

All chess pieces derive from a single abstract base:

```
Piece
 ├── Pawn
 ├── Knight
 ├── Bishop
 ├── Rook
 ├── Queen
 └── King
```

Common data (e.g., color) is shared, while behavior differs per subclass.

### **3.3 Polymorphism**

Each subclass implements its own movement logic through:

```python
def can_move(self, game, sr, sc, tr, tc):
    ...
```

Movement validation is delegated to the specific object type rather than a large conditional block.
This achieves **behavioral specialization** and **clean rule separation**.

### **3.4 Encapsulation**

Chess rules—including:

* Move legality
* Attack mapping
* King-safety checks
* Special-move rules
* Board mutation during simulation

are encapsulated within the `ChessGame` class, preventing UI components from accessing internal states directly.

### **3.5 Exception Handling**

Structured exception handling prevents crashes and handles invalid operations gracefully (e.g., invalid move attempts or missing user inputs).

### **3.6 Dictionary Usage**

Dictionaries are used to manage:

* Piece symbols
* Castling rights
* Promotion options
* Player configurations
* Page navigation settings

---

## **4. AI System**

Two levels of AI are implemented:

### **Club-Level AI**

* Random legal move selection
* Beginner-friendly gameplay

### **World-Champion AI**

* Material-based board evaluation
* Move scoring and selection
* Simple heuristic resembling classical chess engine evaluation

---

## **5. Project Structure**

This project intentionally follows a **single-file architecture** to satisfy academic requirements:

```
Python Project.py     # Complete application
README.md             # Project documentation
```

Despite being a single file, the code is organized into logical sections:

* Piece classes
* Core game engine
* Move validation system
* UI pages and widgets
* AI modules
* Utility functions

---

## **6. Running the Application**

### **Requirements**

* Python **3.11+**
* Tkinter (bundled with Python on Windows/macOS)

### **Command**

```bash
python "Python Project.py"
```

---

## **7. Building an Executable (Optional)**

Install PyInstaller:

```bash
pip install pyinstaller
```

Build a standalone executable:

```bash
pyinstaller --onefile "Python Project.py"
```

Output will appear in the `dist/` directory.

---

## **8. Screenshot Suggestions**

Add screenshots to enhance the repository:

```

```

---

## **9. License**

This project is intended for academic and personal use.
Feel free to modify and extend the application.

---

## **10. Author**

Developed by **San Win**
Software Engineering Student
KMITL — Thailand

---

If you want, I can also generate a **beautiful GitHub banner**,
or a **class diagram** to include in your README.
