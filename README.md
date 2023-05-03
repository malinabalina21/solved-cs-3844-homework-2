Download Link: https://assignmentchef.com/product/solved-cs-3844-homework-2
<br>
Homework #2 – Convert C to Assembly

CS 3844 Section 0B1,

Given this C program:

#include &lt;stdio.h&gt;




int main(int argc, char *argv[]) {

int i;

printf(“Hex  Dec  Oct   Ch
”);

for (i=32; i&lt;256; i++) {

printf(” %2x  %3d  %3o   %c
”, i, i, i, i);

}

}

Output should look like this (from both the C program above and your Assembly version):

Convert it to Assembly (inside C). You must use Visual Studio in the VDI. If you run it on Linux, characters 128 to 255 won’t show up.

#include &lt;stdio.h&gt;

#include &lt;stdlib.h&gt;




int main(int argc, char *argv[]) {

char *hdr = “Hex  Dec  Oct   Ch
”;

char *msg = “%3x  %3d  %3o   %c
”;




__asm {

TBD

}

system(“pause”);

}

Replace the TBD with two parts: a loop on EAX from 32 to 255, and a function. You must do a CALL to your function and RET to return. And you must pass in the loop variable to the function using the EAX register.

Hint: Use the command “call printf” to do the two prints. It expects all the parameters on the Stack. What order do the parameters need to be to printf?