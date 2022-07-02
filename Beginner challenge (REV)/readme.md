### Chall Desc:
Dust of the cobwebs, let's reverse.

### Soln

We are given a zip file.

Using `unzip` command, we can unzip the file and we get a file `a.out`.

Using `file` command, we confirm that it is a 64 bit binary file (`ELF`).

```py
chmod +x a.out
./a.out

# The program asks us for a flag as input. On wrong answer, we get a failure message. 
Use binary ninja or ghidra to view the program of binary.

We see
