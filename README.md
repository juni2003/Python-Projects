# 🐍 Python Projects — Detailed Project Guide

A curated collection of mini Python projects created as learning exercises. Each script is self-contained and demonstrates fundamental concepts: control flow, randomness, file I/O, simple GUIs (turtle), and terminal interaction. This README gives a short description and usage notes for each project.

---

## ⚙️ Requirements
- Python 3.8+ recommended.
- Optional packages used by some projects:
  - colorama (pip install colorama)
  - windows-curses (Windows, for curses support)
- Desktop environment required for turtle-based project.
- Note: Some scripts use platform-specific features (e.g., winsound on Windows).

---

## ▶️ Quick start
1. Clone:
   git clone https://github.com/juni2003/Python-Projects.git
2. (Optional) Create & activate virtual env.
3. Install dependencies if needed:
   pip install colorama
   pip install windows-curses   # only on Windows if running Typing_Master
4. Run any script:
   python "Guess_Number_Game.py"
   (Use quotes for filenames with spaces.)

---

## 🗂 Projects

### Adventure Story Game — Advanture_Story_Game.py 🧭
A text-based, branching narrative that asks the player to make choices (left/right, swim/walk, hide/flee, etc.) which lead to different outcomes. Uses time.sleep to pace the story and create suspense. Great for beginners learning conditional flow and simple input handling. Note: filename contains a minor typo ("Advanture").

### Dice Dash Game — Dice Dash Game.py 🎲
A multiplayer turn-based dice game for 2–4 players. Players roll to accumulate points; rolling a 1 resets the turn score, and rolling a 6 gives +10 points and ends the turn. First to reach the target (default 50) triggers a final round. Uses colorama for colored terminal feedback and simple input loops.

### Guess the Number — Guess_Number_Game.py 🔢
Classic high-low guessing game where the user picks an upper bound and gets five tries to guess a random number. Includes input validation and helpful hints ("Try a higher/lower number") after incorrect attempts. Good for practicing loops, user input, and random number generation. Lightweight and ideal for beginners.

### High-Low Game — High_Low_Game.py ⬆️⬇️
Shows a current number and asks the player to predict whether the next randomly chosen number (0–10) will be higher or lower. Correct guesses add to the score; a wrong guess ends the game and shows the final score. Uses colorama for clearer success/failure messages. Demonstrates loop control and basic game state.

### Madlib TaleMaker — Madlib TaleMaker.py ✍️
Reads a `story.txt` file and extracts placeholders like `<noun>` or `<verb>`, prompts the user to provide replacements, and prints the completed story. Offers an option to save the final version to a new file. Excellent example of file I/O, regex-safe replacement (re.escape + re.sub), and string parsing. Ensure `story.txt` exists in the same folder.

### Maths Problem Quest — Maths Problem Quest.py ➗
A timed 10-question math quiz with three difficulty levels (Easy/Medium/Hard) that set operand ranges. Problems use random operators (+, -, *) and the script tracks wrong answers; exceeding the allowed wrong attempts ends the quiz. Measures completion time and provides basic colored feedback via colorama. Useful for practicing random generation, validation, and simple timing.

### Quiz Game — Quiz game.py ❓
A short quiz focused on computer science acronyms (10 questions). Expects full-phrase answers (case-insensitive), and provides a final performance message based on the score. Simple structure; good for demonstrating input handling, scoring, and conditional output. Consider adding synonyms/alternate accepted answers to improve robustness.

### Rock Paper Scissors — Rock_Paper_Scissors_Game.py ✊✋✌️
Play against the computer until a chosen score limit is reached. Each round compares the player's choice against a random computer pick and updates win/loss counts. Uses colorama for colored result messages. Quick fix: the options list currently contains a typo — change `["rock","paper","paper"]` to `["rock","paper","scissors"]`.

### Slot Machine — Slot Machine.py 🎰
A console-based slot machine simulator with simple betting mechanics: deposit, choose lines, place bets, and spin. Symbols have different counts and values; matching rows yield payouts. Includes lightweight animations (delays) and balance tracking. Great for practicing lists, dictionaries, random sampling, and user-driven game loops.

### Time Conversion (12→24) — Time_convertion_12-hours_to_24-hours_format.py ⏰
Converts times in the "HH:MM:SS AM/PM" format into 24-hour format. Validates basic structure and hour range, then adjusts hours for AM/PM rules (e.g., 12 AM → 00). Ideal as a small utility exercise in string slicing and simple validation. Enhancement: stricter minute/second validation (0–59) is recommended.

### Turtle Speedway Game — Turtle_Speedway_Game.py 🐢
Graphical racing game using Python's turtle module. Players choose how many racers and which turtle colors to bet on; turtles race vertically and the script prints the winning bettor. Draws a finish line and displays player names near their chosen turtles. Requires a desktop environment (won't run on headless servers) and is a nice intro to GUI animation in Python.

### Typing Master — Typing_Master.py ⌨️
Terminal-based typing speed & accuracy test built with curses. Loads random lines from Typing_Master.txt, times the user, computes WPM and accuracy, and plays keypress sounds (winsound on Windows). Key notes: the loader currently references `"Tying_Master.txt"` (typo) — change it to `"Typing_Master.txt"`. Also, curses require OS support (install `windows-curses` on Windows). Useful for learning curses, terminal UI, and text handling.

---

## ⚠️ Notable quick fixes (one-liners)
- RPS options: options = ["rock", "paper", "scissors"]
- Typing loader: open("Typing_Master.txt", "r")
- Rename files to remove spaces for easier CLI use (e.g., Dice_Dash_Game.py)
- Consider replacing winsound with a cross-platform audio library if you need portability.

---

## ✨ Recommended next steps
- Add requirements.txt for quick installs (e.g., colorama, windows-curses).
- Standardize file names (snake_case, no spaces) and fix minor typos.
- Add simple unit tests for pure functions (timeConversion, slot payout logic).
- Add brief example `story.txt` for Madlib and sample input README snippets for the turtle game.

---

## 🤝 Contributing
Fork → branch → PR with focused changes. Include short descriptions and basic tests where applicable. Prefer cross-platform fixes and keep interactive behavior intact.

---

## 📝 License & metadata
- Consider adding a LICENSE (MIT recommended) to clarify reuse permissions.
- Repo: https://github.com/juni2003/Python-Projects
