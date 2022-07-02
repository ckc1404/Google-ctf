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
```
![](https://user-images.githubusercontent.com/95117634/176989878-88c9112d-1f19-49e4-a8de-04805831efb6.png)

We see that it first asks for an input and then scans 15 bytes of data via `scanf`. 

SSE - Streaming SIMD Extensions is a single instruction, multiple data (SIMD) instruction set extension to the x86 architechture.

Now, in our program we have three more operations - Xor, shuffle and add.
