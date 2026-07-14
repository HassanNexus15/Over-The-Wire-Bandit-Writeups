# Bandit Level 4

## Objective

The password for the next level is stored in the only human-readable file in the `inhere` directory.

---

## How It Was Solved

1. I first listed the contents of the current directory using `ls` and found a directory named `inhere`.
2. I changed into the `inhere` directory using the `cd` command.
3. I used the `find` command to list all the files inside the directory.
4. Since I did not yet know how to identify a human-readable file automatically, I manually opened each file using the `cat` command.
5. Most of the files contained unreadable binary data, so I continued checking each one until I found the file containing readable text.
6. The readable file contained the password for the next level.

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
cat ./-file00
cat ./-file01
cat ./-file02
cat ./-file03
cat ./-file04
cat ./-file05
cat ./-file06
cat ./-file07
cat ./-file08
cat ./-file09
```

---

## Key Takeaways & Lessons Learned

- The `find` command can be used to list every file inside a directory.
- Not every file contains readable text; some files store binary data that appears as random characters when viewed with `cat`.
- Testing different files one by one can help narrow down the correct file when a better method is not yet known.
- Every challenge teaches multiple ways to solve the same problem, and experimenting is an important part of learning Linux.

---

## Password Obtained Successfully and Used to Access the Next Level

*(Password intentionally omitted for ethical reasons.)*
