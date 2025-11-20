Sam@el’s Chess

A Complete Python & Tkinter Chess Application








Overview

Sam@el’s Chess is a full-featured chess engine and graphical user interface built in Python using Tkinter, designed to run entirely in a single file.
It implements complete chess rules, multiple game modes, AI opponents, and a structured UI—making it ideal for academic submission, practical gameplay, and portfolio showcase.

This project demonstrates clear Object-Oriented Programming (OOP) design, strong separation of logic and UI, and clean architectural organization inside a unified codebase.

Features
✔ Gameplay

Player vs Player (Local)

Player vs AI (Two difficulty levels)

Legal move highlighting

Move history tracking window

Captured pieces display

Optional time controls (Unlimited / 5 / 10 / 30 minutes)

✔ Fully Implemented Chess Rules

All legal movement patterns

Castling (Queen-side & King-side)

En Passant

Pawn Promotion

Check, checkmate, and stalemate detection

King-safety validation

Illegal move prevention

✔ User Interface (Tkinter)

Multi-page navigation (Menu → Mode → Game)

Dark-mode inspired theme

Dynamic board rendering

Click-based piece selection

Scrollable Learn Chess educational module

Smooth window transitions

Architecture & Design
Object-Oriented Structure
Piece (Base Class)
 ├── Pawn
 ├── Knight
 ├── Bishop
 ├── Rook
 ├── Queen
 └── King

Key Principles

Inheritance: All pieces extend Piece

Polymorphism: Each piece implements its own can_move(...)

Encapsulation: Internal board state controlled by ChessGame

Composition: ChessGame owns board, move rules, captured lists, rights

Dictionary Usage: Symbol mapping, castling rights, promotions, routing

Exception Handling: Prevents crashes from invalid actions

AI System
Club-Level AI

Random but legal move selection

Suitable for beginners

Strong AI

Material-based evaluation

Weighted scoring (Queen > Rook > Bishop > Knight > Pawn)

Selects best move based on board advantage

Project Structure (Single-File Layout)

Even in one file, the codebase is cleanly segmented into:

• Chess Piece Classes
• Core Chess Engine (ChessGame)
• Move Validation System
• AI Modules
• Tkinter GUI Pages
• Utility Functions & Constants


This layout ensures clarity, readability, and extensibility.

Installation
Requirements

Python 3.11+

Tkinter (bundled with Windows/macOS Python)

Run
python "Python Project.py"


The main menu will load automatically.

Build as Executable (Optional)
pip install pyinstaller
pyinstaller --onefile "Python Project.py"


Executable appears in the dist/ directory.

License

This project is intended for personal, academic, and learning use.
Modification and extension are allowed.

Author

San Win
Software Engineering Student
KMITL — Thailand
