Download Link: https://assignmentchef.com/product/solved-ece3790-lab4-huffman-coding-and-lu-decomposition
<br>
<strong>The purpose of this lab is to give you practical coding experience. </strong>It will also reinforce concepts we’ve covered in class.

<strong>Important: </strong>Please include the following signed statement with your submission.

I (We), [insert name(s)] attest that the work I am (we are) submitting is my (our) own work and that it has not been copied/plagiarized from online or other sources. Any sourced material used for completing this work has been properly cited. [Signature(s)]

<strong>Also Important: </strong>Labs done in pairs must be submitted with a short paragraph outlining each partner’s contribution.

<h1>Introduction</h1>

This lab covers two class topics and allows you to reinforce concepts by implementing solutions. The lab also gives you practical experience in two important areas: 1) working from someone else’s code and 2) Matlab.

<h1>Problem 1 – Huffman Coding</h1>

In class we went through the process of generating Huffman Codes for a file. The program Lab 4 Problem 1 Huffman.py is an incomplete implementation of a Huffman function library (encode/decode). The program uses two python modules: heapq (for the priority queue) and bitstring (for manipulating bitstrings). Your job is to complete the code.

<h2>Functions</h2>

<ol>

 <li>Complete the function getfilecharactercounts. It should return a list of unique characters that occur in the file (excluding those that don’t occur in the file).</li>

 <li>Complete the function createhuffmantree by processing the min priority queue (core part of the Huffman Algorithm; see Lecture 18 for pseudocode).</li>

 <li>Complete the function huffmanencodefile. This function already produces the bitstring for you but has not written it to file. You will need to think carefully about what else should be added to the file so that it can be decoded, and how to handle the case when the bitstring is not an even number of bytes.</li>

 <li>Write the function huffmandecodefile. This function should read a huffman encoded file.</li>

</ol>

<strong>Important: </strong>Think carefully about what you will put in your encoded file in order to make decoding easier. We will have some friendly competition for bonus marks here (more below).

<h2>Main Program</h2>

Complete the main program. It should read the provided file, encode the file, decode the file, and verify that the file was properly decoded.

<h2>Analysis</h2>

Working on other people’s code can be uncomfortable if you aren’t used to it, but it is great practice and happens a lot in industry. We won’t do any standard data analysis in this part of the lab, but you are to include a short writeup that:

<ul>

 <li>Provide a high-level overview of how the entire program works (key steps, associated functions).</li>

 <li>Explains the functionality of the HuffmanNode class (include a description of members and member functions).</li>

 <li>Explain what the createhuffmantree, codehuffmantree, and huffmanencodefile functions do and how they do it.</li>

</ul>

<h2>Evaluation and Discussion</h2>

Answer the following questions:

<ol>

 <li>Explain the process you used to convert the encoded bitstring back into the original data. What information did you include in your file to enable decoding? Why did you choose the information you did?</li>

 <li>What was the size of your compressed file, and what compression ratio (uncompressed:compressed size) did you achieve. Are you happy with this? Why or why not?</li>

 <li>What file content would lead to the highest possible compression ratio for this coding scheme? What is the compression ratio limit of this scheme? Justify your answers.</li>

 <li>Is Huffman coding used in practice? If so for what purposes. If not, why not? Support you answers with references.</li>

</ol>

<h2>Bonus</h2>

There is a single bonus available to the group/individual that submits the solution that provides the smallest compressed file. Of course the file must be 1) compressed using Huffman Coding, 2) decoded using your huffmandecodefile function, 3) not resort to semantic arguments (e.g., “you said we had to use our function to decode the file but you didn’t say that function couldn’t just read the file again to get the decoded file”). In essence these limitations imply that the bonus is available for the group that keep additional information in the file as lean as possible. The bonus will be worth 2% of your total <em>lab mark </em>(over all 5 labs), not to exceed 100% of the total course lab mark. We’ll also crown you champions of the 2nd annual ECE 3790 Huffman Coding Challenge in class (assuming you want me to, no cash value, and no actual crown will be awarded).

<strong>Hand in:</strong>

All codes, your analysis writeup, answers to the discussion questions, and your compressed file.

<h1>Problem 2 – LU Decomposition</h1>

In this problem we will implement LU decomposition factorization and solve routines in Matlab. We are going to force you to use Matlab (or Octave) as it is good practice. We are also going to force you to use Matlab vector operations and subarray indexing (slicing) as it is also good practice.

<h2>Functions</h2>

<ol>

 <li>Implement a function called LUDecomposition that, given a square matrix <em>A</em>, returns the LU decomposition of <em>A</em>. Your function should only be two nested for loops. This implies that the third for loop (over entries in a given row) should be implemented using Matlab vector operations. Recall that the “:” operator can be used to refer to or extract portions of a matrix/vector.</li>

 <li>Implement a function called LUSolve that, given <em>L </em>and <em>U </em>and right-hand-side vector <em><u>b</u></em>, solves the system of equations and returns the solution <em><u>x</u></em>. Use vector operations wherever possible.</li>

</ol>

<h2>Main Program</h2>

Write a main program Lab 4 Problem 2 that:

<ul>

 <li>Randomly generates an <em>n</em>×<em>n </em>matrix and 5 right-hand-side vectors. Produces the LU decomposition (time this) and solves the 5 right-hand-side vectors (time this separately). Remember the Matlab operations tic and toc.</li>

 <li>Validates the solution by using the built-in Matlab routine lu and appropriate solves (you will want to use the Matlab slash operator here – we leave it to you to figure it out). Time the built-in routines separately (like you timed your own routines).</li>

</ul>

<h2>Validation and Data Collection</h2>

Once you have completed writing your functions and main program you need to:

<ul>

 <li>Show that your functions work.</li>

 <li>Use your functions to collect timing data for various matrix sizes and plot the timing data compared to the theoretical complexity of the elimination and substitution steps.</li>

</ul>

<h2>Evaluation and Discussion</h2>

Answer the following questions:

<ol>

 <li>Describe your system speed and RAM. Given your code, what is the largest system you could get into RAM and solve? Justify your answer. Assuming RAM wasn’t an issue, what problem size could you solve in 1 hour? (Hint: don’t actually do this.) How much RAM would that problem take?</li>

 <li>Based on the timing results you obtained (for factoring the matrix and solving 5 righthand-sides for some specific matrix size <em>n</em>) what timing results would you have expected to see if you applied Gaussian Elimination instead of LU decomposition? Quantify and justify your answer.</li>

</ol>

<strong>Hand in:</strong>

Hand in all code, plots, and your answers to the discussion questions.