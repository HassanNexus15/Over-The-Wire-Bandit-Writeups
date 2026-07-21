# Bandit Level 12

## Objective

The password for the next level is stored in the file `data.txt`, which contains a hexdump of a file that has been repeatedly compressed.

---

## How It Was Solved

1. I created a temporary working directory under `/tmp` to avoid modifying the original challenge file.
2. I copied `data.txt` into the temporary directory and renamed it to keep the workspace organized.
3. Since `data.txt` contained a hexadecimal representation of a binary file, I reconstructed the original binary using `xxd`.
4. Instead of guessing the next step, I used the `file` command to identify the type of the reconstructed file.
5. Based on the output of `file`, I extracted the file using the appropriate tool (`gunzip`, `bunzip2`, or `tar`).
6. After each extraction, I repeated the process:
   - Identify the file type.
   - Use the correct extraction utility.
   - Inspect the newly extracted file.
7. I continued this investigation until the final extracted file was identified as plain ASCII text.
8. Finally, I displayed the contents of the text file to obtain the password.

---

## Commands Used

```bash
mkdir /tmp/safe
```

```bash
cp data.txt /tmp/safe
```

```bash
cd /tmp/safe
```

```bash
mv data.txt rename.txt
```

```bash
xxd -r rename.txt new-file.bin
```

```bash
file new-file.bin
```

```bash
gunzip -d < new-file.bin > output.txt
```

```bash
file output.txt
```

```bash
bunzip2 -c output.txt > decompressed.txt
```

```bash
file decompressed.txt
```

```bash
gunzip -d < decompressed.txt > second.txt
```

```bash
file second.txt
```

```bash
tar -xvf second.txt
```

```bash
file data5.bin
```

```bash
tar -xvf data5.bin
```

```bash
file data6.bin
```

```bash
bunzip2 -c data6.bin > third.txt
```

```bash
file third.txt
```

```bash
tar -xvf third.txt
```

```bash
file data8.bin
```

```bash
gunzip -d < data8.bin > fourth.txt
```

```bash
file fourth.txt
```

```bash
cat fourth.txt
```

---

## Key Takeaways & Lessons Learned

- The `file` command is one of the most valuable Linux utilities for identifying unknown file types.
- Hexdumps can be converted back into their original binary form using `xxd -r`.
- Different compression formats require different extraction tools, such as `gunzip`, `bunzip2`, and `tar`.
- When dealing with unfamiliar files, it is better to inspect them first rather than guessing which command to use.
- Breaking a problem into small investigation steps makes complex tasks much easier to solve.
- Working inside `/tmp` provides a safe location for temporary files without modifying the original challenge data.

---

## Challenges Faced

One of the biggest challenges was understanding that the file had been compressed multiple times using different formats. I initially tried viewing binary files with `cat`, which produced unreadable output. By using the `file` command after every extraction, I developed a systematic workflow instead of relying on trial and error.

I also encountered several commands (`xxd`, `bunzip2`, `tar`) that were new to me. I referred to Linux documentation and online resources to understand their purpose before applying them to the challenge.

---

## Password Obtained Successfully and Used to Access the Next Level

*(Password intentionally omitted for ethical reasons.)*
