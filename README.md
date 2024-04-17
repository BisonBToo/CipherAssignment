The purpose of this assignment is to give you some practice using vi, git, github, and a compiler/interpreter(i.e. Python, C++, or C) from the command line (CLI). You are probably used to using a nice Integraded Development Environment (IDE) like MSCode, or Atom, Repl.it. In some cases you may not have those software engineering tools available. Also, if you want to engage the open source community, you should be comfortable with using the CLI.
You will implement a Simple Ceasar Cipher. It is one of the simplest techniques for data encryption and decryption. The idea of a Caesar cipher is this: you encode a message by shifting each letter some number of places. Thus, if the shift is 2, then A becomes C, B becomes D, and so on. Like this:
.guides/img/letter-shift
Surprisingly, you can do this by simply doing arithmetic with characters. Since characters are represented as ASCII numbers, simple addition and subtraction should work straight forward. For example, if a char in a string contains the value ‘A’ (i.e. 65 ASCII), then ‘A’ + 2 gives the value ‘C’ (i.e. 67 ASCII). Unfortunately, (‘Z’ + 2) does not give you the letter ‘B’ (you can see why from the picture above), but if you realize you went past 'Z’, you can subtract 26 (so the result is ‘Z’ + 2 - 26, or ‘Z’ - 24), and this will give you 'B’. Another way to implement this if you are using an alphabet lookup array is to use the modulus operator (i.e. ‘Z’ + (2 % 26)).
This also means that if you encode a message with a shift of n, you can decode it with another shift of 26 - n. n is called the encryption key, and 26 - n would be the decryption key. Anyone who posses these keys, and the alphabet could break your code. Obviously, this approach can be easily broken, but this assignment is meant to be fun, give you some exposure to coding directly using the CLI, and a simple example of cryptography and how it is used in cybersecurity.
