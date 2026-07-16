# Bandit Level 8

## Objective

The password for the next level is stored in the file `data.txt` and is the only line of text that occurs only once.

---

## How It Was Solved

1. I first listed the contents of the home directory and found the `data.txt` file.
2. My initial attempt was to use the `uniq -u` command directly on the file, but it did not produce the expected result.
3. I then experimented with the `sort` command and learned that `uniq` only compares adjacent lines.
4. After sorting the file, duplicate lines were placed next to each other.
5. Finally, I piped the sorted output into `uniq -u`, which displayed the only line that appeared exactly once. That line contained the password for the next level.

---

## Commands Used

```bash
ls
```

```bash
sort data.txt
```

```bash
uniq -u data.txt
```

```bash
sort data.txt | uniq
```

```bash
sort data.txt | uniq -u
```

---

## Key Takeaways & Lessons Learned

- The `uniq` command only removes or identifies **adjacent** duplicate lines.
- If duplicate lines are scattered throughout a file, `uniq` cannot detect them correctly.
- The `sort` command arranges identical lines next to each other, making `uniq` work as intended.
- The pipe operator (`|`) allows the output of one command to become the input of another, making command combinations much more powerful.
- Understanding how individual Linux commands work together is just as important as learning the commands themselves.

---

## Password Obtained Successfully and Used to Access the Next Level

*(Password intentionally omitted for ethical reasons.)*
