# Transformation

**Category:** Reverse Engineering <br>
**Author**: MARK E. HAASE

_I wonder what this really is..._ [enc](https://mercury.picoctf.net/static/a757282979af14ab5ed74f0ed5e2ca95/enc)

`''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)])`

1. Download the “enc” file
2. Use `cat` to see what’s in it. It will output a decoded string.
3. Using [Cyberchef](https://gchq.github.io/CyberChef/), I’ll try decoding it (feel free to use any online decoder or even using a Python Script)<br>
Here’s something really handy in CyberChef. Choose magic and it’ll decode automatically without you needing to specify what algorithm it uses.
4. Didn't get the flag instantly, I’ll try using intensive mode.And there you go! Turns out it was encoded with UTF-16BE.

#### Flag:  picoCTF{16_bits_inst34d_of_8_d52c6b93}