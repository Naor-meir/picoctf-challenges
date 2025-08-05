# Challenge: wave a flag

**Category**: General Skills  
**Points**: 💯  (easy)
**Description**:  
A binary file provides a hint when executed. Can you figure out how to interact with it correctly and reveal the flag?

---

## 🧪 Approach

When I ran the binary without any arguments, it printed:

```
Hello user! Pass me a -h to learn what I can do!
```

This message clearly hinted that the binary supports a help flag (`-h`), which is a common pattern in CLI tools.

Upon executing the binary with `-h`, I received the following response:

```
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_18788aaa}
```

---

## 🛠️ Commands Used

```bash
./warm
./warm -h
```

---

## ✅ Flag

```
picoCTF{b1scu1ts_4nd_gr4vy_18788aaa}
```

---

## 🧠 Takeaways

- Always pay attention to hints in program output — they often guide you directly to the next step.
- Many binaries (especially in CTFs) support common flags like `-h` or `--help`.
- Not every challenge requires reverse engineering — sometimes it's about thinking like a hacker, not coding like one.

---

## 🔗 References
- [`CLI Flags`](https://en.wikipedia.org/wiki/Command-line_interface#Options)

