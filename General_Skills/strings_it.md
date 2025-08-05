# Challenge: strings it

**Category**: General Skills  
**Points**: 💯  
**Description**:  
A binary file contains a hidden flag. Your task is to extract it using command-line tools.

---

## 🧪 Approach

I used the `strings` command to extract all printable character sequences from the binary file.  
To ensure full coverage of the file (including non-initialized or non-loaded sections), I included the `-a` flag.  
To reduce noise, I filtered only strings of length ≥ 4 using the `-n` flag, and used `grep` to locate the flag.

---

## 🛠️ Commands Used

```bash
strings -a -n 4 strings | grep picoCTF
```

- `-a` → Scan the entire file, not just loaded sections    
- `grep picoCTF` → Look specifically for lines containing the flag

---

## ✅ Flag

```
picoCTF{5tRIng5_1T_d66c7bb7}
```
---

## 🧠 Takeaways

- `strings` is a quick and effective tool for identifying readable content in binary files.
- Use `-a` to avoid missing strings in non-standard sections.
- Pairing `strings` with `grep` is a useful method for narrowing down CTF flags.
- Always try variations like different encodings (`-e l`), or adjusting `-n` to tune your results.

---

## 🔗 Resources

- [`man strings`](https://linux.die.net/man/1/strings)  
