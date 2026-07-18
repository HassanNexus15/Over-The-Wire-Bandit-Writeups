# Bandit Level 11

## Objective

The password for the next level is stored in the file `data.txt`, where all lowercase (`a-z`) and uppercase (`A-Z`) letters have been rotated by 13 positions (ROT13).

---

## How It Was Solved

1. I first listed the contents of the home directory using the `ls` command and found the `data.txt` file.
2. I displayed the contents of the file using the `cat` command and noticed that the text appeared to be encoded.
3. Since the challenge description mentioned that the letters had been rotated by 13 positions, I researched the **ROT13** cipher and learned that it is a simple substitution cipher.
4. I discovered that the `tr` command can be used to translate one set of characters into another.
5. Using the `tr` command, I translated every uppercase and lowercase letter by 13 positions, which decoded the message and revealed the password for the next level.

---

## Commands Used

```bash
ls
```

```bash
cat data.txt
```

```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

---

## Key Takeaways & Lessons Learned

- ROT13 is a simple substitution cipher that rotates every alphabetical character by 13 positions.
- The `tr` command is used to translate or replace characters from one set to another.
- The pipe operator (`|`) allows the output of one command to become the input of another command.
- Understanding basic encoding and substitution techniques is useful in Linux and cybersecurity.
- Researching unfamiliar concepts before solving a challenge helps build a deeper understanding of the underlying technology.

---

## Password Obtained Successfully and Used to Access the Next Level

*(Password intentionally omitted for ethical reasons.)*
