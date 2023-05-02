Download Link: https://assignmentchef.com/product/solved-comp348-assignment2-lisp-language
<br>
In this assignment you will be practicing functional programming using Lisp language.

<h2><a name="_Toc5106"></a>2.1            List Processing</h2>

For the following questions, implement the function in lisp. Some examples are provided to illustrate the behaviour of each function. Note that Your implementation must work for all form of possible inputs.

Q 1. Write a lisp function that takes a list and an integer n, and returns the last n elements of the list, as a new list, e.g.:

&gt; (take-n ’(1 2 3) 2)

(2 3)

In case n is less than 1, it returns NIL. In case n is beyond the length, the function returns a copy of the original list.

Q 2. Write a function called reverse-cut-in-half that receives a list and creates a new list whose elements are the rst and the second halves reversed. e.g.:

&gt; (reverse-cut-in-half ’(1 2 3))

((3) (1 2))

&gt; (reverse-cut-in-half ’((1) (2) (3) (4)))

(((3) (4)) ((1) (2)))

In case of odd length, the        rst half before reversing takes the middle element.

Show the output for (reverse-cut-in-half ’(a))

<h2><a name="_Toc5107"></a>2.2            Structures</h2>

Q 3. Write a lisp function that receives a list as the input argument (the list is mixed up integers, decimals, characters and nested lists) and returns a attened list containing all the atomic elements that are numbers, without any duplication. Sample function output is shown below:

(flatten ’(1 2 (3 1) (a 2.5) (2 4.5) ((1 2))))

(1 2 3 2.5 4.5)

Note that the elements are given in the same order as they are received.

Partial marks are given if the order is not maintained.

Q 4. Write a lisp program to check whether a binary tree is a Binary Search Tree. A Binary Search Tree (BST) is a tree in which all the nodes follow the below-mentioned properties:

The left sub-tree of a node has a key less than or equal to its parent node’s key.

The right sub-tree of a node has a key greater than to its parent node’s key.

The list representing the structure of a sample binary tree is given in the following:

’(8 (3 (1 () ()) (6 (4 () ())(7 () ()))) (10 () (14 (13) ())))

Q 5. Write a function called balancedp that takes a structure and returns true if it is balanced. A structure is balanced if number of elements and all their subelements on the left hand side is equal to the number of elements and all their subelements on the right hand side. e.g.:

&gt; (balancedp ’(a b c))

T

&gt; (balancedp ’(a b c d))

T

&gt; (balancedp ’(hello world (this is a test))) ; outer list

NIL                                                                                                           ; has 3 elements

&gt; (balancedp ’(hello world (this assingment))) ; outer list

NIL                                                                                                           ; has 3 elements

&gt; (balancedp ’((1 2) (3 (1)))

T

<h2><a name="_Toc5108"></a>2.3            Miscellaneous Programs</h2>

Q 6. Write a lisp function triangle that takes an integer as the argument and prints a triangle of stars as shown in the following gure. If the input is 0, decimal or string, it should print an appropriate error message. positive integers print left-justi ed triangles, whereas for the negative numbers the printed triangles are right-justi ed.

Example:

&gt; (triangle 2.5) invalid number; please enter a positive or a negative integer

&gt; (triangle 0) invalid number; please enter a positive or a negative integer

Q 7. The 3<em>x</em>+1 Conjecture: The Collatz conjecture 1931

Let <em>T </em>be the transformation that sends an even integer <em>x </em>to <em>x/</em>2 and an odd integer <em>x </em>to 3<em>x</em>+1. For all positive integers <em>x</em>, when we repeatedly apply the transformation <em>T</em>, we will eventually reach the integer 1.

<ul>

 <li>Write a function collatz that takes n as its argument and <u>returns </u>a list with the sequence from n to 1.</li>

</ul>

In case of invalid inputs, the function returns NIL, as well as displaying error message to the output. Examples of invalid inputs is n not being a positive number. You are not allowed to use any builtin functions except predicate functions to check value type.

&gt; (collatz 4)                                               &gt; (collatz 3)

(2 1)                                                               (10 5 16 8 4 2 1)

&gt; (collatz 10)

(5 16 8 4 2 1)

&gt; (collatz 30)

(15 46 23 70 35 106 53 160 80 40 20 10 5 16 8 4 2 1)

<ul>

 <li>Using the above function, write a short code to print the colattz list for numbers from1 to 20.</li>

</ul>