# APDS TP1: What I Understood

My own summary of the TP1 lecture for **Advanced Programming for Data Science (APDS)**,
written as a LaTeX Beamer slide deck.

- **Student:** HEM Bellyday
- **Department:** Applied Mathematics and Statistics (AMS), Institute of Technology of Cambodia (ITC)
- **Lecturer:** Mr. VANN Visal
- **Lecture date:** October 13, 2026

## Files

| File | Description |
| --- | --- |
| `apds_tp1_summary.tex` | LaTeX Beamer source of the slides |
| `apds_tp1_summary.pdf` | Compiled slides (11 pages, 16:9) |
| `README.md` | This file |

## What the slides cover

1. **Part 1: Building Blocks.** What a function, variable, class, method, module,
   package, and constant are.
2. **Part 2: Clean Code.** What clean code is, plus descriptive names, comments,
   docstrings, naming values that don't change, and clear functions.
3. **Part 3: PEP 8.** What PEP 8 is, the naming styles, the main rules in simple
   words, and a before/after code example.
4. **Part 4: Debugging.** What debugging is, the tools the teacher recommended, and
   how I debug (printing suspicious lines and splitting code into files).

## Summary of the slides

### Part 1: Building Blocks

- **Function:** This is like a math function: it has something like x or y in it
  when we define it. We use it so we don't do a task again and again; we just use
  this function and finish. (Write once, use quickly.)
- **Variable:** A variable is like a math definition: it refers to a value or
  object when we want to define it.
- **Class:** A class is like a function, but it has a bunch of functions inside
  of it.
- **Method:** A method is a function that makes something work, or does an
  action, inside a class. Example on the board: calculate score.
- **Module:** A module is like a `.py` file: we write functions inside it and call
  them to use in the future in another module.
- **Package:** A bunch of modules stuck together. When we install a package, that
  is a bunch of modules ready to use.
- **Constant:** It refers to a value that doesn't change, even in future use.

### Part 2: Clean Code

Before clean code, the teacher asked what is something in class we don't
understand, and I said PEP 8.

**Clean code** refers to a file or code lines written so that not only the user
can understand them, but others can too.

- **Descriptive name:** name the variable so it can be understood quickly, and
  keep it short. Example: a function to start a moto engine; there are many names
  we could use, but use one name that other functions in the moto can't use.
- **Comment:** `#` that explains code in a single line.
- **Docstring:** used to explain a whole function or class so others can
  understand it.
- **Naming values:** name values that can't be changed (even in the future they
  don't change), so it is easy and we don't have to find that value in whatever
  file it is in.
- **Functions:** a function needs to be clear and reasonable to use.

### Part 3: PEP 8

PEP 8 is created by Python itself, just to make code structure more clean and
reasonable, and it is also a rule to follow from Python.

| What | Style | Example |
| --- | --- | --- |
| Variables, functions, methods | `snake_case` | `student_score` |
| Constants | `UPPER_CASE` | `PASS_MARK` |
| Classes | `PascalCase` | `Student` |

PEP 8 rules in simple words:

- **Indentation:** 4 spaces for each level.
- **Line length:** at most 79 characters for code, 72 for comments and docstrings.
- **Imports:** put them at the top. First Python's built-in modules, then
  installed libraries, then my own files, with a blank line between each group.
  Don't use `from x import *`.
- **Spaces:** one space around `=` and `==`, but no extra space just inside
  brackets or before the `(` of a call.
- **Commas and colons:** a space after a comma, like `[60, 80]`, but no spaces in
  a slice, like `scores[1:3]`.
- **Blank lines:** 2 between top-level functions or classes, 1 between methods
  inside a class.
- **Long lines:** wrap them inside parentheses, and break the line before an
  operator like `+` or `and`.
- **Quotes:** choose `'` or `"` and keep using the same one. Docstrings use `"""`.

Example:

```python
# Not following PEP 8
passmark=50
def HasPassed( s ):
  return s>=passmark
print (HasPassed(75))
```

```python
# Following PEP 8
PASS_MARK = 50


def has_passed(score):
    return score >= PASS_MARK


print(has_passed(75))
```

### Part 4: Debugging

**Debugging** is fixing errors, of course. But sometimes the error shown is not
clear or reasonable, so we have to check further in the code file.

The teacher recommended 2 old-school tools. Even before AI existed, these are
what old programmers used. (I forgot the names.)

How I debug:

1. Print the suspicious code line, so we can clearly see the error and know what
   to fix.
2. Don't put 5 million lines of code in 1 file. Divide them and use them as
   imports. When there is an error, it is easy to find in the file structure.

That's all I learned from that day.

## How to compile

You need a LaTeX distribution with Beamer (TeX Live, MiKTeX, or Overleaf).

```bash
pdflatex apds_tp1_summary.tex
pdflatex apds_tp1_summary.tex   # run twice so the outline is filled in
```

On Overleaf, upload `apds_tp1_summary.tex` and click **Recompile**.

## Packages used

`beamer` (Madrid theme, beaver color theme), `listings` for the Python code,
`booktabs` for the table, and `xcolor`.
