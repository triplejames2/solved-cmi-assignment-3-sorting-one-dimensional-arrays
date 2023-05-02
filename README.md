Download Link: https://assignmentchef.com/product/solved-cmi-assignment-3-sorting-one-dimensional-arrays
<br>
Create an ARMv8 assembly language program that implements the following algorithm:

#define  SIZE 50

int main()

{

int v[SIZE], i, j, min, temp;




/*  Initialize array to random positive integers, mod 256  */

for (i = 0; i &lt; SIZE; i++) {

v[i] = rand() &amp; 0xFF;

printf(“v[%d]: %d
”, i, v[i]);

}




/*  Sort the array using a selection sort  */

for (i = 0; i &lt; SIZE – 1; i++) {

/*  Find the least element in the right subarray  */

min = i;

for (j = i + 1; j &lt; SIZE; j++) {

/*  Compare elements  */

if (v[j] &lt; v[min])

min = j;

}




/*  Swap elements  */

temp = v[min];

v[min] = v[i];

v[i] = temp;

}




/*  Print out the sorted array  */

printf(“
Sorted array:
”);

for (i = 0; i &lt; SIZE; i++)

printf(“v[%d]: %d
”, i, v[i]);




return 0;

}




Create space on the stack to store all local variables, using the techniques described in lectures. Use <em>m4</em> macros or assembler equates for all stack variable offsets. Optimize your code so that it uses as few instructions as possible. Be sure, however, that you always read or write memory when using or assigning to the local variables. Name the program <em>assign3.asm</em>.




Also run the program in <em>gdb</em>, first displaying the contents of the array before sorting, and then displaying it again once the sort is complete (use the <em>x</em> command to examine memory). You should show that the algorithm is working as expected. Capture the <em>gdb</em> session using the <em>script </em>UNIX command, and name the output file <em>script.txt</em>.




<strong>Other Requirements</strong>




Make sure your code is readable and fully documented, including identifying information at the top of each file. You must comment each line of assembly code. Your code should also be well designed:  make sure it is well organized, clear, and concise.




<strong>New Skills Needed for this Assignment:</strong>




<ul>

 <li>Use of the stack to store local variables</li>

 <li>Addressing stack variables</li>

 <li>Use of <em>m4</em> macros or assembler equates for stack variable offsets</li>

 <li>Storing and addressing one-dimensional arrays on the stack</li>

</ul>