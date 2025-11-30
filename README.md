# 🐍 Python Projects — Polished & Concise README

A curated set of small Python projects built as learning exercises. Each script is self-contained and demonstrates fundamentals: control flow, randomness, file I/O, simple GUIs (turtle), and terminal interaction.

---

## ⚙️ Requirements
- Python 3.8+
- Install common deps:
  - pip install colorama
  - On Windows for curses: pip install windows-curses
- Optional (cross-platform sound): simpleaudio or playsound
- Desktop environment required for turtle-based project.

---

## ▶️ Quick start
1. Clone:
   git clone https://github.com/juni2003/Python-Projects.git
2. (Optional) Create & activate venv.
3. Install deps (see Requirements).
4. Run a script:
   python "Guess_Number_Game.py"
   (Use quotes for filenames that contain spaces.)

---

## 🗂 Project summary (short & actionable)
- Advanture_Story_Game.py — Text-based branching adventure (note: filename typo "Advanture") 🧭
- Dice Dash Game.py — Turn-based dice race for 2–4 players (colorama) 🎲
- Guess_Number_Game.py — Guess the secret number within limited attempts 🔢
- High_Low_Game.py — Predict whether the next number is higher/lower (colorama) ⬆️⬇️
- Madlib TaleMaker.py — Fill placeholders from story.txt to create a madlib ✍️
- Maths Problem Quest.py — 10-question timed math quiz (3 difficulties, colorama) ➗
- Quiz game.py — Short CS acronyms quiz; expects exact phrase answers ❓
- Rock_Paper_Scissors_Game.py — Classic RPS vs CPU (fix: options list contains typo) ✊✋✌️
- Slot Machine.py — Betting & spin simulation with payouts 🎰
- Time_convertion_12-hours_to_24-hours_format.py — Convert "HH:MM:SS AM/PM" → 24h ⏰
- Turtle_Speedway_Game.py — Graphical turtle race; players bet on colors (requires GUI) 🐢
- Typing_Master.py (+ Typing_Master.txt) — Terminal typing speed & accuracy test (curses, winsound) ⌨️

---

## ⚠️ Notable issues & quick fixes
- Rock_Paper_Scissors_Game.py:
  - options = ["rock","paper","paper"] → should be ["rock","paper","scissors"].
- Typing_Master.py:
  - load_text() opens `"Tying_Master.txt"` by mistake. Change to `"Typing_Master.txt"`.
  - winsound is Windows-only — wrap import in try/except or use cross-platform audio.
- Madlib TaleMaker.py:
  - Requires a `story.txt` with placeholders like `<noun>`.
- Filenames with spaces: consider renaming (e.g., Dice_Dash_Game.py) for easier CLI usage.
- Advanture_Story_Game.py: filename typo ("Advanture" → "Adventure") — optional rename.
- Time conversion: current validation could be stricter for minutes/seconds (0–59).

---

## ✨ Suggested small improvements
- Add requirements.txt for one-line installs.
- Standardize filenames (snake_case, no spaces).
- Replace platform-specific sound (winsound) with cross-platform alternative.
- Add argparse-based non-interactive modes for easier testing.
- Add unit tests for pure functions (e.g., timeConversion).

---

## 🤝 Contributing
- Fork → branch → PR with focused changes.
- Include tests where practical and check cross-platform behavior (Windows vs macOS/Linux).
- Prefer small, well-documented commits.

---

## 📝 License & metadata
- Consider adding an explicit LICENSE (e.g., MIT) if you want reuse permissions.
- Repo: https://github.com/juni2003/Python-Projects
