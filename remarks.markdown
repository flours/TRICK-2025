This is a Quine-like program that prints pi (π)

```bash
ruby entry.rb
```

I confirmed the following implementations/platforms:

* ruby 3.3.5 (2024-09-03 revision ef084cc8f4) [arm64-darwin23]

### Description

This program displays the digits of pi one by one as ASCII art.
Each frame of ASCII art contains an embedded executable program that generates the next digit of pi.

### Internals

This program contains ASCII art data for the digits 0 to 9 and '.'.
The data is compressed using run-length encoding (RLE), where each digit is represented by a single-character identifier to minimize storage.

### Limitation

* the program use escape sequence for move cursor, which may not be supported in some terminal environments.
* this program circulated 80 digits of pi, so it can't calculate more than 80 digits.
