# Bandit Level 9

## Objective

The password for the next level is stored in the file `data.txt` in one of the few human-readable strings, preceded by several `=` characters.

---

## How It Was Solved

1. I first listed the contents of the home directory using the `ls` command and found the `data.txt` file.
2. Since the challenge mentioned that the password was stored in one of the few human-readable strings, I researched commands that could extract readable text from binary files.
3. Through the Linux documentation and online resources, I learned about the `strings` command, which displays printable text contained within a file.
4. I combined the `strings` command with `grep` to search specifically for lines containing the `=` characters mentioned in the objective.
5. The matching line contained the password for the next level.

---

## Commands Used

```bash
ls
```

```bash
strings data.txt | grep "="
```

---

## Key Takeaways & Lessons Learned

- The `strings` command extracts printable, human-readable text from binary files.
- The `grep` command can be combined with other commands using a pipe (`|`) to filter specific output.
- Reading the challenge description carefully often provides clues about which Linux commands to use.
- Researching unfamiliar commands is an important part of learning Linux and cybersecurity.
- Combining simple Linux commands can solve problems much more efficiently than using a single command.

---

## Password Obtained Successfully and Used to Access the Next Level

*(Password intentionally omitted for ethical reasons.)*
