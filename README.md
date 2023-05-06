Download Link: https://assignmentchef.com/product/solved-ecgr3180-assignment-1
<br>



<ol>

 <li> The following problem involves the design of an unsigned hexadecimal/hex (base-16) to decimal (base-10) converter. The conversion can be done using the decimal equivalent of each hex digit multiplied by the weight of the digit. More information on the conversion and a calculator can be found at: <a href="https://www.binaryhexconverter.com/hex-to-decimal-converter">https://www.binaryhexconverter.com/hex</a><a href="https://www.binaryhexconverter.com/hex-to-decimal-converter">–</a><a href="https://www.binaryhexconverter.com/hex-to-decimal-converter">to</a><a href="https://www.binaryhexconverter.com/hex-to-decimal-converter">–</a><a href="https://www.binaryhexconverter.com/hex-to-decimal-converter">decimal</a><a href="https://www.binaryhexconverter.com/hex-to-decimal-converter">–</a><a href="https://www.binaryhexconverter.com/hex-to-decimal-converter">converter</a> All variable names will be given in double quotes in the prompt below to ensure all variables are named correctly.</li>

</ol>

Design a singly linked list where each node is a char named “value” and has a pointer named “link” pointing to the next node in the list. The link of the last node in the list points to NULL. Write code for the following:

<ul>

 <li>The struct described above, name it “digit”.</li>

 <li>A class named “hex” to implement a singly-linked list that will contain any number of nodes, dependent on how many digits the user enters. The user will enter the hex digits one at a time and press the Enter key after every digit. When done, the user will enter ‘-‘ to signify the end of the linked list.</li>

 <li>When a new digit is entered, it will be stored as a node at the end of the linked list. Create a function named “addDigit” that will implement this functionality.</li>

 <li>The hex class will have a private variable named “count” to keep track of the number of nodes in the linked list and increase it every time a new node is added at the end of the list.</li>

 <li>The first node will have a pointer pointing to it named “head” that will never change its pointing. It points to the MOST SIGNIFICANT digit in the hexadecimal number. This will have an exponent value of count-1.</li>

 <li>A function named “convertToDecimal” that will iterate through all hex digits and convert the value to decimal and return it as an int. See the link at the top of this question for the procedure. The basic procedure is to multiply the hex digit (or its decimal equivalent if above 9) by the weight of each digit (this will be 16 “to the power of” the digit location). For example: hex number 2D9E in decimal is: 2*16^3 + D*16^2 + 9*16^1 + E*16^0 = 2*16^3 + 13*16^2 + 9*16^1 + 14*16^0 = 11678.</li>

 <li>The user may enter only valid hex digits (0 through F), no other input is allowed. If the value entered by the user is invalid, output an error message to the console and store the number entered so far without the invalid input.</li>

</ul>




<strong>class hex </strong>

<strong>{ </strong>

<strong>     private:       struct digit </strong>

<strong>          { </strong>

<strong>               // YOUR CODE GOES HERE </strong>

<strong> </strong>

<strong>          }; </strong>

<strong> </strong>

<strong>          // ANY ADDITIONAL CODE GOES HERE </strong>

<strong> </strong>

<strong>     public: </strong>

<strong> </strong>

<strong>          // MOST, IF NOT ALL, FUNCTIONS GO HERE </strong>

<strong> </strong>

<strong>}; </strong>

<strong> </strong>

<strong>/***********************************************************/ </strong>

<strong> </strong>

<strong>#include &lt;iostream&gt; </strong>

<strong> using namespace std; </strong>

<strong> </strong>

<strong>int main()  </strong>

<strong>{ </strong>

<strong>      </strong>

<strong>     // WRITE TEST CODE HERE, THE MORE TESTS THE BETTER. </strong>

<strong>     // ADD COMMENTS FOR EACH TEST CASE. </strong>

<strong>      </strong>

<strong>} </strong>

<ol start="2">

 <li> The following problem involves the design of function to merge multiple vectors using iterators. For more information and references to use the vector container, see <a href="http://www.cplusplus.com/reference/vector/vector/">http://www.cplusplus.com/reference/vector/vector/</a> or any other reference. This function will require the use of an iterator to traverse the vector.</li>

</ol>

<ul>

 <li>Write a function (named “mergeVectors”) that will take in user input for a list of integers for each vector and output a merged vector to the console. The user will first enter a list of vectors as an array of vectors and then merging will occur. For an example of an array of vectors</li>

</ul>

— The first value requested as user input is the number of vectors that will be entered. This number must be larger than 0. Include a checkpoint for this in your code and do no advance until proper input is given.

— The code will then request for the user to enter the values in each vector. The values will be nonnegative. If the user enters a negative value (such as -1 or more negative), the function will stop taking user data for the current vector and move to asking for data for the next vector in the array (entering a negative value essentially means the user is done entering data for the given vector.)

— Populate the array with vectors (possibly of different sizes, depending on user input) using the approach described above.

<ul>

 <li>After the array of vectors has been populated with user data, iterate through every element in the array of vectors and output the elements to the console using the following algorithm:</li>

</ul>

— The code will output the elements at index [0] for all vectors, then for index [1] if available, etc.

— If a vector is shorter than the current index to be output, it will be skipped during output and the code will move to the next vector in the array, etc. See the examples below on how this merging will occur.




——————————————————————————

Example 1:

If the user has entered all of the vectors below as part of your code (this is just showing the vectors, not how they are stored), then the merging will be as follows:




v1 = [1, 2, 3, 4] v2 = [5, 6, 7, 8]




Console output:

1, 5, 2, 6, 3, 7, 4, 8




———————————–




Example 2: (spacing is added in this example for readability)




v1 = [1,  2,  3, 4, 9, 10] v2 = [5,  6,  7, 8] v3 = [9, 10, 11]




Console output:

1, 5, 9, 2, 6, 10, 3, 7, 11, 4, 8, 9, 10




———————————–




Example 3: (spacing is added in this example for readability)




v1 = [1,   2,  3,  4,  9, 10, 11]

v2 = [5,   6,  7,  8] v3 = [9,  10, 11]

v4 = [11, 12, 13, 14, 19, 20]




Console output:

1, 5, 9, 11, 2, 6, 10, 12, 3, 7, 11, 13, 4, 8, 14, 9, 19, 10, 20, 11




/*******************************************************************/




<strong>#include &lt;iostream&gt; </strong>

<strong> </strong>

<strong>using namespace std; </strong>

<strong> </strong>

<strong>void mergeVectors(); </strong>

<strong> </strong>

<strong>int main()  </strong>

<strong>{     </strong>

<strong>     //Testing your code </strong>

<strong>     mergeVectors(); </strong>

<strong>} </strong>

<strong>/*******************************************************************/  </strong>

<strong>// YOUR FUNCTION mergeVectors GOES HERE. IT WILL BE OF TYPE void AND TAKE NO ARGUMENTS. ALL OPERATIONS WILL TAKE PLACE IN THIS FUNCTION. </strong>




<ol start="3">

 <li>(20 pts) For each one of the loops below, give a Big-Oh analysis of the running time. Show work/reasoning.</li>

</ol>




<ol>

 <li><strong>sum = 0; for (i = 0; i &lt; n; ++i) </strong></li>

</ol>

<strong>++sum; </strong>

<strong> </strong>

<ol>

 <li><strong>sum = 0; for (i = 0; i &lt; n; ++i) for (j = 0; j &lt; n; j++) </strong></li>

</ol>

<strong>++sum; </strong>




<ol>

 <li><strong>sum = 0; for (i = 0; i &lt; n; ++i) for (j = 0; j &lt; n</strong><strong>n; ++j) </strong></li>

</ol>

<strong>++sum; </strong>




<ol>

 <li><strong>sum = 0; for (i = 0; i &lt; n; ++i) for (j = 0; j &lt; i; ++j) </strong></li>

</ol>

<strong>++sum; </strong>




<ol>

 <li><strong>sum = 0; for (i = 0; i &lt; n; ++i) for (j = 0; j &lt; i </strong><strong>i; ++j) for (k = 0; k &lt; j; ++k) </strong></li>

</ol>

<strong>++sum; </strong>

<ol>

 <li><strong>sum = 0; for (i = 1; i &lt; n; ++i) for (j = 1; j &lt; i </strong><strong>i; ++j) if (j % i == 0) for (k = 0; k &lt; j; ++k) </strong></li>

</ol>

<strong>++sum; </strong>