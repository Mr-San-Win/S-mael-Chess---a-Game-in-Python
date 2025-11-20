Sam@el’s Chess — A Python & Tkinter Chess Application

Sam@el’s Chess is a fully-functional chess application developed in Python using Tkinter and implemented entirely within a single code file.
The project demonstrates clean Object-Oriented Programming (OOP) design, complete chess rule implementation, user-friendly graphical interfaces, and basic AI opponents.

The system is designed for both academic assessment and practical gameplay and includes an integrated Learn Chess module for beginners.

1. Overview

This application provides a structured and interactive chess experience featuring:

Two game modes (PvP and Human vs AI)

A multi-page Tkinter GUI

Complete enforcement of chess rules

A modular OOP logic layer decoupled from the UI

Move history, captured pieces tracking, and time controls

Educational resources for new players

The project complies with formal software development requirements and demonstrates the application of OOP concepts within a single-file architecture.

2. Key Features
Gameplay

Player vs Player (Local)

Human vs AI

Club-Level AI (random but legal)

Strong AI (evaluation-based)

Highlighted legal moves

Move history window

Captured piece display

Time control options (No limit, 5/10/30 minutes)

Chess Rules (All Implemented)

Legal movement validation

Castling (complete rules)

En Passant

Pawn Promotion

Check, checkmate, stalemate

Illegal move prevention

King-safety verification

User Interface (Tkinter)

Multi-frame navigation

Clean dark-mode theme

Responsive board rendering

Click-based piece selection

“Back to Menu” navigation

Integrated instructional page (“Learn Chess”)

Scrollable content sections

3. Object-Oriented Architecture

The project meets academic OOP requirements through a clean and expressive design.

3.1 Composition

The central class ChessGame owns:

The 8×8 board of Piece objects

Game state attributes

Captured piece lists

Move history

Castling/en-passant rights

3.2 Inheritance
Piece
 ├── Pawn
 ├── Knight
 ├── Bishop
 ├── Rook
 ├── Queen
 └── King

3.3 Polymorphism

Each subclass implements its own movement logic via:

def can_move(self, game, sr, sc, tr, tc):
    ...

3.4 Encapsulation

All chess rules and state logic are self-contained within ChessGame.

3.5 Exception Handling

Used to prevent crashes during invalid operations.

3.6 Dictionary Usage

Dictionaries are used for:

Piece symbols

Castling rights

Promotion options

Player configurations

Page navigation settings

4. AI System
Club-Level AI

Random selection among all legal moves

Beginner-friendly

Strong AI

Material-based evaluation

Move scoring and decision making

5. Project Structure

This project follows a single-file architecture for academic requirements:

Python Project.py     # Complete application
README.md             # Documentation


Logical sections include:

Piece classes

Game engine

Move validation system

GUI pages

AI modules

Utility functions

6. Running the Application
Requirements

Python 3.11+

Tkinter (comes with Python on Windows/macOS)

Run Command
python "Python Project.py"

7. Building an Executable (Optional)

Install PyInstaller:

pip install pyinstaller


Build:

pyinstaller --onefile "Python Project.py"


Executable appears in dist/.

8. License

This project is intended for academic and personal use.
You may modify or extend it freely.

9. Author

Developed by San Win
Software Engineering Student
KMITL — Thailand
