Download Link: https://assignmentchef.com/product/solved-ceng462-artificial-intelligence-homework-1
<br>
<h2>1      Objectives</h2>

This assignment aims to assist you to expand your knowledge on informed search in the cases of A* and Iterative Deepening A* algorithms.

<h2>2       Problem Definition</h2>

In this assignment, you are going to solve a given N-puzzle by using A* and Iterative Deepening A* algorithm.

You already know what N-puzzle is, but just to refresh your memory, here is the definition of N-puzzle:

<em>N-puzzle </em>is a game consisting of a <em>k </em>x <em>k </em>board with <em>N </em>= <em>k</em><sup>2</sup>−1 sliding tiles and a blank space where the aim is to reach a specific configuration from a given configuration by moving the tiles near the blank space.

Here is an example of initial and goal configurations for 8-puzzle (where k = 3) from the textbook:

(a) initial state                                  (b) goal state

Figure 1: Example configurations as initial and goal states for 8-puzzle (taken from [1])

<h1><a name="_Toc8581"></a>3      Specifications</h1>

<ul>

 <li>You are going to implement A* and Iterative Deepening A* algorithms (you can refer the lecture slides for pseudocodes.) in python.</li>

 <li>You will use the <strong>total Manhattan distance </strong>as the heuristic function. For instance, it is 18 for the example given in Section 2.</li>

 <li>The task will be given from standard input and the result will be printed to standard output.</li>

 <li>Input will consist of:

  <ul>

   <li>the method you are going to use for the given task (“A*” or “IDA*” for Iterative Deepening A*)</li>

   <li>M as the maximum total estimated cost allowed in the method</li>

   <li>k defining the dimension of board,</li>

   <li>the initial configuration of the board, <strong>– </strong>the goal configuration of the board.</li>

  </ul></li>

 <li>Output will consist of “SUCCESS” or “FAILURE” stating whether the goal is reached or not respectively. If the solution exists, all configurations on the path from the initial configuration to the goal configuration will be printed as well.</li>

 <li>While expanding a node you are required to try to move <strong>up</strong>, <strong>down</strong>, <strong>left</strong>, <strong>right </strong>in that order (Moving up means sliding the tile below the blank upward, similar for other directions.)</li>

 <li>When searching for the state with the minimum cost you will select the <strong>first </strong>one for tie-breaking.</li>

</ul>

<strong>IMPORTANT NOTE: </strong>Last two items are crucial for the black-box evaluation. Please avoid any violation of them, in order not to lose any points redundantly.

<h2>4       Sample I/O</h2>

<strong>Input 1:</strong>

A∗

50

3

3 2 5

<ul>

 <li>4 1</li>

 <li>_ 8 _ 1 2</li>

</ul>

3 4 5

6 7 8

<strong>Output 1:</strong>

SUCCESS

3 2 5

<ul>

 <li>4 1</li>

 <li>_ 8</li>

</ul>

3 2 5

6 4 1

_ 7 8

3 2 5

_ 4 1

6 7 8

<ul>

 <li>2 5</li>

 <li>_ 1</li>

</ul>

6 7 8

3 2 5 4 1 _ 6 7 8

3 2 _ 4 1 5

6 7 8

<ul>

 <li>_ 2</li>

 <li>1 5</li>

</ul>

6 7 8

3 1 2 4 _ 5

6 7 8

3 1 2 _ 4 5

6 7 8

_ 1 2

3 4 5

6 7 8

<strong>Input 2:</strong>

IDA∗

50

3

3 2 5

<ul>

 <li>4 1</li>

 <li>_ 8 _ 1 2</li>

</ul>

3 4 5

6 7 8

<strong>Output 2:</strong>

SUCCESS

3 2 5

6 4 1 7 _ 8

3 2 5

<ul>

 <li>_ 1</li>

 <li>4 8</li>

</ul>

3 2 5 6 1 _ 7 4 8

3 2 _ 6 1 5

7 4 8

<a href="#_Toc8581">3                                                                                                                                                                                                                         2</a>

<a href="#_Toc8582">6 1                                                                                                                                                                                                                     5</a>




7 4 8

3 1 2 6 _ 5

7 4 8

3 1 2

<ul>

 <li>4 5</li>

 <li>_ 8</li>

</ul>

3 1 2

6 4 5

_ 7 8

3 1 2 _ 4 5

6 7 8

_ 1 2

3 4 5

6 7 8

<strong>Input 3:</strong>

A∗ 20

4

2 1 3 4

5 6 7 8

9 10 11 12 13 14 15 _

1 2 3 4

5 6 7 8

9 10 11 12 13 14 15 _

<strong>Output 3:</strong>

FAILURE

<strong>Input 4:</strong>

IDA∗

20

3

1 2 3

4 5 6 7 8 _

1 2 3

4 5 6 8 7 _

<strong>Output 4:</strong>

FAILURE

<h2>5      Regulations</h2>

<ol>

 <li><strong>Programming Language: </strong>You must code your program in Python. Your submission will be tested in inek machines. So make sure that it can be executed on them.</li>

 <li><strong>Implementation: </strong>You have to code your program by only using the functions in standard module of python. Namely, you <strong>cannot </strong>import any module in your program. The only exception for this rule is the copy module which may be useful with the deepcopy function to cope with aliasing list problem in python.</li>

 <li><strong>Late Submission: </strong>No late submission is allowed.</li>

 <li><strong>Cheating: We have zero tolerance policy for cheating</strong>. People involved in cheating (any kind of code sharing and codes taken from internet included) will be punished according to the university regulations.</li>

 <li><strong>Discussion: </strong>You must follow the OdtuClass for discussions and possible updates on a daily basis.</li>

 <li><strong>Evaluation: </strong>Your program will be evaluated automatically using “black-box” technique so make sure to obey the specifications. A reasonable timeout will be applied according to the complexity of test cases in order to avoid infinite loops due to an erroneous code.</li>

</ol>

<h1><a name="_Toc8582"></a>6      Submission</h1>

Submission will be done via OdtuClass system. You should upload a <strong>single </strong>python file named in the format <em>&lt;</em><strong>your-student-id</strong><em>&gt; </em><strong>hw1.py </strong>(i.e. e1234567 hw1.py).

<h2>References</h2>

[1] S. J. Russell and P. Norvig, <em>Artificial intelligence: a modern approach</em>. Malaysia; Pearson Education Limited,, 2016.