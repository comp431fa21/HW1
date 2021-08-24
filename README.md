# HW1 

** Please let the TAs know on Piazza if something is unclear or amiss in this repo! **

## Developing in Python
If you are new to Python, do not despair!  Picking up a new programming language is not as hard as the first time.  Be sure to look for some tutorials online.  [Python's official website](https://wiki.python.org/moin/BeginnersGuide/NonProgrammers) has lots of links to good resources under the "Interactive Courses" header.

Once you get a feel for the basics, start thinking about how to discover more efficient ways of programming in Python.  For example, while coding this assignment, you may find that you would like to know if a particular string or character consists only of alphabetical characters- what would your search engine query look like if you wanted to know if Python has a built-in mehtod for determining this?  w3schools.com has any easily navigable compilation of [Python's built-in features](https://www.w3schools.com/python/python_reference.asp).

## Connecting to the Course Server
In order to connect to the course server, you must either be connected on campus physically (via eduroam) or virtually (via the Cisco AnyConnect VPN).  Once this connection is established, open your terminal and input ```ssh <YOUR ONYEN>@comp431fa21.cs.unc.edu```.  Be sure to replace <YOUR ONYEN> with your onyen.  You will be prompted for a password; enter your typical UNC onyen password.  Let the TA's know if you are having trouble with this.

## Testing Your Code
Once you are ready to more rigorously test your parser, clone or otherwise download exmapleInputs.txt and exampleExpectedOutputs.txt from this repo into your HW1 folder.  The input file has the five example inputs given in the assignment instructions; the output file has the corresponding outputs.

To test your program with the inputs and compare your results with the expected outputs, first open your terminal and enter ```python3 parser.py < exampleInputs.txt > myOutputs.txt```.  Next, enter ```expectedExampleOutputs.txt diff myOutputs.txt > outputDiff.txt```.  The first command feeds the input file into your parser and saves the results in a file named "myOutputs.txt".  The second command compares your actual outputs with the expected outputs and saves the difference in a file named "outputDiff.txt".
  
When your program is working as expected, outputDiff.txt will be empty.  Otherwise, every line where the two files differ will be annotated.  For example, you may see something like this in outputDiff.txt:
  ```
8c8
< ERROR -- mailbox
---
> ERROR -- local part
10c10
< ERROR -- path
---
> ERROR -- domain
```
The "8c8" signifies the line number of difference (8).  The line directly underneath shows "< ERROR -- mailbox", which signifies that the leftmost compared file (as entered in the command line; expectedExampleOutputs.txt in our case) produced "ERROR -- mailbox" on line 8.  The line below that, showing "> ERROR -- local part", means the rightmost compared file produced "ERROR -- local part" instead.  
  
Use these sample inputs and outputs as a starting point.  We will test you on many more permutations than the five given.  And don't forget about the newline characters!
