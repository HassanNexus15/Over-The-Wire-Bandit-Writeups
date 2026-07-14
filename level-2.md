# Bandit Level 2

## Objective

The password for the next level is stored in a file called `--spaces in this filename--` located in the home directory.

---

## How It Was Solved

1. I first searched for **"spaces in filename"**, as suggested in the **Helpful Reading** section on the OverTheWire Bandit website.
2. After reading the documentation, I experimented with a few different command combinations on my own.
3. I learned that filenames containing spaces must either be enclosed in quotation marks or have each space escaped using a backslash (`\`).
4. Using the correct syntax, I successfully displayed the contents of the file and obtained the password.

---

## Commands Used

```bash
cat "./--spaces in this filename--"
