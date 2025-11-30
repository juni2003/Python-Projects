# 🐍 Python Projects — polished README

Welcome — this repository collects a set of small Python projects created as learning exercises. Each project is a self-contained Python script that demonstrates core programming concepts: control flow, user I/O, randomness, file handling, simple GUIs (turtle), and terminal interaction.

This README replaces the original README with a more detailed, professional, and actionable single-file guide covering:
- What each project does
- Requirements and compatibility notes
- How to run each project (examples)
- Known issues and recommended fixes
- Suggested improvements and contribution guidelines

---

## Table of contents
- Repository overview
- Global requirements & environment
- How to run (clone + prepare)
- Per-project details (purpose, inputs, run command, notes)
  - Adventure Story Game
  - Dice Dash Game
  - Guess Number Game
  - High-Low Game
  - Madlib TaleMaker
  - Maths Problem Quest
  - Quiz Game
  - Rock Paper Scissors Game
  - Slot Machine
  - Time conversion (12 → 24)
  - Turtle Speedway Game
  - Typing Master
- Known issues & quick fixes
- Suggested enhancements
- Contribution, license & contact

---

## Repository overview
Repository: juni2003/Python-Projects  
Description: A collection of mini Python projects (games, utilities, learning exercises).

Files included (main Python scripts):
- Advanture_Story_Game.py
- Dice Dash Game.py
- Guess_Number_Game.py
- High_Low_Game.py
- Madlib TaleMaker.py
- Maths Problem Quest.py
- Quiz game.py
- Rock_Paper_Scissors_Game.py
- Slot Machine.py
- Time_convertion_12-hours_to_24-hours_format.py
- Turtle_Speedway_Game.py
- Typing_Master.py
- Typing_Master.txt (data for typing test)
- README.md (this file)

---

## Global requirements & environment
- Python 3.8+ recommended.
- Install dependencies used across various scripts:
  - colorama (used in several terminal games)
  - windows-curses (only on Windows if you want to run curses-based programs)
  - For Windows-only sound: winsound is built-in (Windows). For cross-platform audio consider packages like playsound or simpleaudio.
- GUI:
  - turtle (standard library) — requires a desktop environment (won't run in headless servers).
- Terminal:
  - curses (used by Typing_Master) — on Linux/macOS it's typically available. On Windows, install `windows-curses` via pip.
- To install dependencies:
  - pip install colorama
  - On Windows, pip install windows-curses
  - (Optional) pip install simpleaudio playsound if you add cross-platform sound.

---

## How to run (quick start)
1. Clone the repository:
   git clone https://github.com/juni2003/Python-Projects.git
   cd Python-Projects

2. (Optional) Create virtual environment:
   python -m venv .venv
   source .venv/bin/activate   # macOS / Linux
   .venv\Scripts\activate      # Windows

3. Install dependencies:
   pip install colorama
   # On Windows for curses-based Typing_Master:
   pip install windows-curses

4. Run any script:
   python "Guess_Number_Game.py"
   (Wrap file names with spaces in quotes, or rename files to remove spaces.)

Note: Many scripts include the line `input("Press Enter to exit...")` — this pauses the program so your terminal window does not immediately close.

---

## Per-project details

### 1) Adventure Story Game
- File: Advanture_Story_Game.py
- Type: Text-based interactive story (branching choices)
- How to run:
  python "Advanture_Story_Game.py"
- Interaction: The game prompts for the player's name and a sequence of choices (left/right, walk/swim, etc.). Each choice leads to different outcomes.
- Notes:
  - Purely text-driven; uses time.sleep to create pacing.
  - Spelling: filename is "Advanture_..." (typo of "Adventure") — consider renaming.

### 2) Dice Dash Game
- File: Dice Dash Game.py
- Type: Turn-based dice game (2–4 players)
- Dependencies: colorama
- How to run:
  python "Dice Dash Game.py"
- Rules overview: players roll; 1 resets turn score, 6 adds 10 points and ends turn. First to 50 triggers final round.
- Notes:
  - Uses colorama for colored terminal output.
  - Handles input errors for number of players.

### 3) Guess Number Game
- File: Guess_Number_Game.py
- Type: Classic guessing game
- How to run:
  python Guess_Number_Game.py
- Interaction: Choose an upper bound, then guess the random number within 5 tries.
- Notes:
  - Input validation is present to ensure numerical input.

### 4) High-Low Game
- File: High_Low_Game.py
- Type: Predict whether next random number is higher or lower
- Dependencies: colorama
- How to run:
  python High_Low_Game.py
- Interaction: Guess H (higher), L (lower), or Q (quit). Scoring +10 for correct guesses; game ends on an incorrect guess.
- Notes:
  - Range is 0–10; ensures next number != current.
  - Input validation exists.

### 5) Madlib TaleMaker
- File: Madlib TaleMaker.py
- Type: Fill-in-the-blanks story generator
- How to run:
  1) Create a `story.txt` file that contains placeholders in the format `<placeholder>` (e.g., `<noun>`, `<verb>`).
  2) python "Madlib TaleMaker.py"
- Interaction: The script finds placeholders, asks user for substitute words, prints the final story, and offers to save it.
- Notes:
  - The script reads `story.txt` from the current directory; include that file before running.

### 6) Maths Problem Quest
- File: Maths Problem Quest.py
- Type: Timed math quiz (10 problems)
- Dependencies: colorama
- How to run:
  python "Maths Problem Quest.py"
- Interaction: Choose difficulty level 1–3 — affects operand ranges. You have up to 5 wrong answers allowed.
- Notes:
  - Uses eval() on generated expressions (safe here because inputs are generated by the program).
  - Times the quiz and displays elapsed seconds.

### 7) Quiz Game
- File: Quiz game.py
- Type: Short CS acronym quiz (10 questions)
- How to run:
  python "Quiz game.py"
- Interaction: Text prompts expecting full phrase answers (case-insensitive).
- Notes:
  - Answers must match exact phrase spelling (e.g., "central processing unit").
  - Consider adding multiple acceptable answers and trimming whitespace.

### 8) Rock Paper Scissors Game
- File: Rock_Paper_Scissors_Game.py
- Type: Classic rock-paper-scissors vs computer
- Dependencies: colorama
- How to run:
  python "Rock_Paper_Scissors_Game.py"
- Interaction: Enter choices until a score limit is reached (script asks for score limit first).
- Known bug:
  - The `options` list is `["rock","paper","paper"]` — this mistakenly duplicates "paper" and lacks "scissors". Change to `["rock", "paper", "scissors"]`.
- Notes:
  - Input validation exists. Uses colorama for colored results.

### 9) Slot Machine
- File: Slot Machine.py
- Type: Simple slot machine simulation with betting
- How to run:
  python "Slot Machine.py"
- Interaction: Deposit money, choose lines to bet on, bet size, spin. Outcomes print slot rows and winnings.
- Notes:
  - Nice console animations (delays). Uses a small built-in economy (balance, bets).
  - There is a short interactive deposit flow if bets exceed balance.

### 10) Time conversion (12 → 24 hours)
- File: Time_convertion_12-hours_to_24-hours_format.py
- Type: Converts "HH:MM:SS AM/PM" → 24-hour format
- How to run:
  python "Time_convertion_12-hours_to_24-hours_format.py"
- Interaction: Input time string in expected format; validates hour range and AM/PM.
- Notes:
  - Validate input format before running; sample prompt included in script.

### 11) Turtle Speedway Game
- File: Turtle_Speedway_Game.py
- Type: Graphical turtle race; players bet on turtle colors
- How to run:
  python "Turtle_Speedway_Game.py"
- Requirements:
  - Must run in a desktop environment; turtle opens a graphics window.
- Interaction:
  - Choose number of racers (2–10), number of players (2–racers), players pick names and turtle colors, then watch the race.
- Notes:
  - Writes player names on screen and draws a finish line.
  - Not suitable for headless environments / online consoles.

### 12) Typing Master
- File: Typing_Master.py
- Data: Typing_Master.txt (contains sample lines)
- Type: Terminal-based typing speed and accuracy test using curses
- How to run:
  python "Typing_Master.py"
- Requirements:
  - curses support: on Linux/macOS it's present; on Windows install `windows-curses`.
  - The script uses winsound for keypress sounds (Windows-only). On other OSes, sound calls need replacement or conditional imports.
- Known mismatch:
  - The code attempts to open `"Tying_Master.txt"` (typo) in load_text() but the repository has `Typing_Master.txt`. Fix load_text() to open `Typing_Master.txt` (or rename the file).
- Notes:
  - The script expects the terminal size to remain stable; resizing restarts the test.
  - Uses curses; run in a real terminal (not in some IDE consoles).

---

## Known issues & quick fixes (recommended changes)
I reviewed each script and noted small, actionable issues and improvements you can apply. These are safe, minimal edits.

1. Rock_Paper_Scissors_Game.py:
   - Bug: options list is `["rock","paper","paper"]`. Fix:
     options = ["rock", "paper", "scissors"]

2. Typing_Master.py:
   - Bug: load_text() opens `Tying_Master.txt` (typo). Fix to open `Typing_Master.txt`.
   - Platform: winsound is Windows-only; wrap `import winsound` in try/except or replace with a cross-platform library.

3. Madlib TaleMaker.py:
   - Requirement: create a `story.txt` file with placeholders like `<noun>`; otherwise script will fail to open it.

4. File names with spaces:
   - Several files have spaces in their names (e.g., "Dice Dash Game.py", "Slot Machine.py"). Consider renaming to use underscores for easier CLI invocation:
     Dice_Dash_Game.py, Slot_Machine.py, Madlib_TaleMaker.py, etc.

5. Adventure naming:
   - Advanture_Story_Game.py has a typo in the file name ("Advanture" vs "Adventure"). Consider renaming.

6. Typing_Master.py — curses on Windows:
   - On Windows `curses` is not available by default. Install `windows-curses` with pip if you want to run it.

7. Time conversion:
   - Validate full format (HH:MM:SS) more strictly (e.g., check minutes and seconds 0–59).

---

## Suggested enhancements (next steps you or contributors can take)
- Add a single `requirements.txt` for easy install:
  - colorama
  - windows-curses (optional)
  - simpleaudio or playsound (optional cross-platform sound)
- Add unit tests for non-interactive modules (e.g., time conversion function).
- Add command-line options for scripts (argparse) to allow non-interactive modes (useful for testing).
- Standardize filenames (no spaces, consistent snake_case).
- Replace platform-specific code (winsound) with cross-platform audio or conditional imports.
- Containerize or provide a GitHub Actions workflow to run static checks (flake8) or run non-GUI tests.
- Add an examples/ or stories/ folder: e.g., `story.txt` templates for Madlib; sample levels for maths quiz.

---

## Contribution & PRs
Contributions are welcome. If you want to help:
1. Fork the repo.
2. Create a feature branch (e.g., fix/rps-options).
3. Keep commits focused and include a short description of changes.
4. Open a PR with a description of changes and a brief summary of how you tested them.

Please add tests for changes when possible and ensure cross-platform compatibility.

---

## License & contact
- License: Add a license file (recommended: MIT) if you want to allow reuse.
- Author / contact: (Use your GitHub profile or email here)

---

