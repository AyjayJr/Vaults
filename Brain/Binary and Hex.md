# Base 10 vs Base 2

Normal math uses base 10 and act as such:
- Each digit counts up to 9 and when you reach 10 you carry the 1
- Has places 10s, hundreds, thousands, etc.

Binary math uses base 2:
- Each digit counts up to 1 and when you reach 2 you carry the 1
- Has places 2s, 4s, 8s, 16s, etc.
- Each binary place value is called a bit, 8bits makes one byte

# Base 16

Base 2 numbers can become long e.g. 100111000100000 is 20,000 in base 10.

To alleviate this we use base 16 a.k.a **Hexadecimal**

Each hex digit corresponds to 4 bits. **2 hex digits makes one byte**

# In C programming

When writing in C, a number is presumed to be base 10.

To tell the compiler otherwise we do the following:
- Binary must be preceded by a 0b e.g. 0b1101101
- Hex must be preceded by a 0x e.g. 0xA57