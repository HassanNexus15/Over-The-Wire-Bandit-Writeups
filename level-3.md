# Bandit Level 3

## Objective

The password for the next level is stored in a hidden file inside the `inhere` directory.

---

## How It Was Solved

1. I first listed the contents of my current directory using `ls` and found a directory named `inhere`.
2. I changed into the `inhere` directory using the `cd` command.
3. Running `ls` did not display any files, which made me realize the password was likely stored in a hidden file.
4. I experimented with the `find` command using different options until I located the hidden file named `...Hiding-From-You`.
5. Finally, I used the `cat` command to display the contents of the file and obtain the password.

---

## Commands Used

```bash
ls
```

```bash
cd inhere
```

```bash
find . -type f
```

```bash
cat "./...Hiding-From-You"
```

---

## Key Takeaways & Lessons Learned

- The `ls` command does not display hidden files by default.
- Hidden files and directories in Linux begin with a dot (`.`).
- The `find` command is useful for locating files when their exact name or location is unknown.
- The `cat` command can be used to display the contents of a file once it has been located.
- Experimenting with different commands helped me understand multiple ways of finding hidden files.

---

## Password Obtained Successfully and Used to Access the Next Level

*(Password intentionally omitted for ethical reasons.)*
