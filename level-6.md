# Bandit Level 6

## Objective

The password for the next level is stored somewhere on the server and has all of the following properties:

- Owned by user `bandit7`
- Owned by group `bandit6`
- Exactly 33 bytes in size

---

## How It Was Solved

1. I first analyzed the challenge requirements and noticed that the target file could be identified by its **owner**, **group**, and **size**.
2. I initially searched only inside my home directory using the `find` command, but no matching file was found.
3. I realized that the challenge stated the file was stored **somewhere on the server**, so I expanded the search to the entire filesystem by starting the search from the root (`/`).
4. I used the `find` command with filters for the file owner, group owner, and file size.
5. Since searching the entire filesystem produced many **Permission denied** messages, I redirected the error output to `/dev/null` so that only valid search results were displayed.
6. After locating the matching file, I displayed its contents using the `cat` command and obtained the password.

---

## Commands Used

```bash
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
```

```bash
cat /var/lib/dpkg/info/bandit7.password
```

---

## Key Takeaways & Lessons Learned

- The `find` command can search for files based on ownership using the `-user` and `-group` options.
- The `-size` option can be used to search for files with an exact size. The suffix `c` represents bytes.
- `find .` searches only the current directory and its subdirectories, while `find /` searches the entire filesystem.
- Searching the whole filesystem may generate permission errors, which can be hidden by redirecting standard error using `2>/dev/null`.
- Combining multiple search criteria in a single `find` command is an efficient way to locate files with specific attributes.

---

## Password Obtained Successfully and Used to Access the Next Level

*(Password intentionally omitted for ethical reasons.)*
