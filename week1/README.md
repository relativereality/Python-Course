# Week 1 — Python Fundamentals

**Course:** Python Programming — Five-Week Foundations
**Topics:** Variables · Lists · Sets · Dictionaries · Loops · Conditionals · Functions · Git basics

---

## What you'll learn this week

By the end of Week 1 you will be able to:

- Install Python 3 and Visual Studio Code on your Mac
- Configure VS Code with the Python and Pylance extensions
- Work with Python's core data types: strings, integers, floats, and booleans
- Store and manipulate collections using lists, sets, and dictionaries
- Control program flow with `if`/`elif`/`else` and `for`/`while` loops
- Write reusable code with functions
- Save your work to GitHub using `git add`, `git commit`, and `git push`

---

## Files in this folder

| File | Description |
|------|-------------|
| `week1_assignment.ipynb` | Assignment notebook — Music Library Manager |

---

## Assignment — Music Library Manager

A project-based assignment where you build a command-line music library step by step.

**Topics covered:**

| Task | What you practice |
|------|-------------------|
| Task 1 | Create variables, a list, a set, and a dictionary |
| Task 2 | Modify collections — `.append()`, `.remove()`, `.add()`, slicing |
| Task 3 | Loop through data with `for`/`while` and `range()` |
| Task 4 | Use set operators `in`, `&`, and `\|` with conditionals |
| Task 5 | Write and call four reusable functions |
| Task 6 | Commit finished work to GitHub |

**Points:** 100 total &nbsp;|&nbsp; **Estimated time:** 2–3 hours

---

## Getting started

### 1. Set up your virtual environment

Open Terminal in VS Code (`` Ctrl+` ``) and run:

```bash
cd ~/Documents/python-course/week1
python3 -m venv venv
source venv/bin/activate
```

Your prompt will change to show `(venv)` when the environment is active.

> **Every time you reopen Terminal**, run `source venv/bin/activate` again before working.

### 2. Open the notebook

With the venv active, launch Jupyter:

```bash
jupyter notebook week1_assignment.ipynb
```

Or open the file directly in VS Code — it has built-in Jupyter support via the Jupyter extension.

### 3. Work through the tasks

- Read the instructions in each grey Markdown cell
- Write your code in the code cell directly below
- Run each cell with **Shift+Return** to see the output
- Do not edit the final **Self-check** cell — run it last to verify your work

### 4. Submit

When all tasks are complete and the self-check passes:

```bash
cd ~/Documents/python-course
git add .
git commit -m "Week 1 assignment: music library"
git push
```

---

## Quick reference

### Core data types

```python
name     = "Alice"          # str
age      = 25               # int
gpa      = 3.8              # float
enrolled = True             # bool
```

### Collections

```python
songs  = ["Song A", "Song B", "Song C"]   # list  — ordered, allows duplicates
genres = {"Rock", "Jazz", "Pop"}          # set   — unordered, no duplicates
album  = {"title": "Abbey Road",          # dict  — key-value pairs
          "year": 1969}
```

### List slicing

```python
songs = ["A", "B", "C", "D", "E"]

songs[0]     # "A"       — first item
songs[-1]    # "E"       — last item
songs[1:4]   # ["B", "C", "D"]  — index 1 up to (not including) 4
songs[:3]    # ["A", "B", "C"]  — first three
songs[2:]    # ["C", "D", "E"]  — from index 2 to the end
```

### Set operators

```python
a = {"Rock", "Jazz", "Pop"}
b = {"Jazz", "Soul", "Pop"}

"Jazz" in a    # True  — membership test
a & b          # {"Jazz", "Pop"}          — intersection (items in both)
a | b          # {"Rock", "Jazz", "Pop", "Soul"}  — union (all unique items)
```

### Loops

```python
# for loop with range — numbered list starting at 1
for i in range(len(songs)):
    print(f"{i + 1}. {songs[i]}")

# for loop over a dictionary
for key, value in album.items():
    print(f"{key}: {value}")

# while loop
count = 5
while count > 0:
    print(count)
    count -= 1
```

### Functions

```python
def greet(name, greeting="Hello"):
    """Returns a greeting string."""
    return f"{greeting}, {name}!"

print(greet("Alice"))           # Hello, Alice!
print(greet("Bob", "Hi"))      # Hi, Bob!
```

### Git workflow

```bash
git add .                          # stage all changes
git commit -m "your message"       # save a snapshot
git push                           # upload to GitHub
git status                         # check what has changed
git log --oneline                  # view commit history
```

---

## Troubleshooting

**`python3: command not found`**
Python is not installed or not on your PATH. Re-run the installer from python.org and verify with `python3 --version`.

**`source venv/bin/activate` gives an error**
Make sure you created the venv first with `python3 -m venv venv`, and that you are inside the `week1/` folder when you run activate.

**Notebook won't open in Jupyter**
Install Jupyter inside your active venv: `pip install notebook`, then try again.

**VS Code doesn't recognise the venv interpreter**
Open the Command Palette (`Cmd+Shift+P`), type `Python: Select Interpreter`, and choose the option that shows `./venv/bin/python`.

**`git push` asks for a password**
GitHub no longer accepts passwords for `git push`. You need a Personal Access Token. Go to GitHub → Settings → Developer settings → Personal access tokens → Generate new token, then use that token as your password.
