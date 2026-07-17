# Bandit Level 10

## Objective

The password for the next level is stored in the file `data.txt`, which contains Base64 encoded data.

---

## How It Was Solved

1. I first listed the contents of the home directory using the `ls` command and found the `data.txt` file.
2. Since the challenge mentioned that the file contained **Base64 encoded data**, I referred to the **Helpful Reading** section on the OverTheWire Bandit website and researched what Base64 encoding is and how it works.
3. I learned that Base64 is an encoding scheme used to represent binary data as readable text and that it can be decoded using the `base64` command.
4. After understanding the concept, I used the `base64` command with the `-d` option to decode the contents of the file.
5. The decoded output revealed the password for the next level.

---

## Commands Used

```bash
ls
```

```bash
base64 -d data.txt
```

---

## Key Takeaways & Lessons Learned

- Base64 is an **encoding** method, not an encryption method.
- Encoded Base64 data can be decoded using the `base64 -d` command.
- Reading the challenge description carefully can provide hints about which Linux commands to use.
- Researching unfamiliar concepts before attempting a solution helps build a stronger understanding rather than simply memorizing commands.
- Linux provides built-in utilities for working with many common encoding formats.

---

## Password Obtained Successfully and Used to Access the Next Level

*(Password intentionally omitted for ethical reasons.)*
