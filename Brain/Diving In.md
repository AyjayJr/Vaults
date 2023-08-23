Each processor has information about the opcodes and their corresponding instructions in a reference manual made by the manufacturer.

Must familiarize yourself with these to understand which instructions are being executed.

## Viewing Binaries

Hexdump to view the contents of Invaders.h

---
**Note**:
- My output differed from the guide due to my output defaulting to 2-byte words when it should be single byte words.

- [this answer](https://stackoverflow.com/questions/58797575/difference-in-hexdump-output-on-osx-and-linux) helped me understand the issue.

- I learned about the concept of [[Endianess]]

- The 8080 is little endian

- to get the same output as the guide I can simply use: 
```
hexdump -C invaders.h
```

---


