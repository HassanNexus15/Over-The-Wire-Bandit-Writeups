# Bandit Level 5

## Objective

The password for the next level is stored in a file somewhere under the `inhere` directory. The file has the following properties:

- Human-readable
- 1033 bytes in size
- Not executable

---

## How It Was Solved

1. I first listed the contents of the home directory and found the `inhere` directory.
2. I changed into the `inhere` directory using the `cd` command.
3. To understand the directory structure, I listed every file using the `find . -type f` command.
4. Since the challenge provided specific properties of the target file, I searched for files that were exactly **1033 bytes** in size using the `find . -size 1033c` command.
5. I also checked which files were **not executable** using the `find . ! -executable` command.
6. From the search results, I identified the directory containing the matching file and navigated to it.
7. Finally, I displayed the contents of the hidden file using the `cat` command and obtained the password.

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
find . -size 1033c
```

```bash
find . ! -executable
```

```bash
cd maybehere07
```

```bash
cat -- ".file2"
```

---

## Key Takeaways & Lessons Learned

- The `find` command supports searching for files based on different properties such as size, permissions, and file type.
- The `-size` option allows files to be filtered by their exact size.
- The `! -executable` option can be used to exclude executable files from the search.
- Breaking a problem into smaller searches makes it much easier to locate the correct file.
- Reading the challenge requirements carefully helps determine which command options are most useful.

---

## Password Obtained Successfully and Used to Access the Next Level

*(Password intentionally omitted for ethical reasons.)*
