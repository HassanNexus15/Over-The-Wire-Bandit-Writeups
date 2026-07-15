# Bandit Level 7

## Objective

The password for the next level is stored in the file `data.txt` next to the word `millionth`.

---

## How It Was Solved

1. I first listed the contents of the home directory using the `ls` command and found the file `data.txt`.
2. My initial attempt was to search for the word `millionth` using the `grep` command on the current directory (`.`), but I received an error because `.` refers to a directory.
3. I then checked my current working directory using the `pwd` command and realized I needed to search inside the actual file instead of the directory.
4. Finally, I ran the `grep` command on `data.txt`, which displayed the line containing the word `millionth` along with the password.

---

## Commands Used

```bash
ls
```

```bash
grep -n "millionth" .
```

```bash
pwd
```

```bash
grep -n "millionth" /home/bandit7
```

```bash
grep "millionth" data.txt
```

---

## Key Takeaways & Lessons Learned

- The `grep` command searches the contents of files, not directories.
- The dot (`.`) represents the current directory, so using `grep` directly on it results in an error unless recursive options are used.
- The `pwd` command helps verify the current working directory when troubleshooting.
- Reading error messages carefully often provides clues about what went wrong.
- The `grep` command is an efficient way to locate specific text within large files.

---

## Password Obtained Successfully and Used to Access the Next Level

*(Password intentionally omitted for ethical reasons.)*
