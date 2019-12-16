# rover
**Mars Rover Instructions**

** Running Rover Program: **
Open rover.html in a browser.

**Basic Rover Instructions:**

Step 1. Choose the starting grid x and y values, then click the button next to it.
Step 2. Choose the starting position and facing, then click the button next to it.
Step 3. Put in your command on the third line and click the button next to it to send commands to the rover.

You can enter commands one by one or as a group of commands.
Any invalid commands will be ignored.  
The directions will rotate all the way around.
If you go out of bounds it will show an error, but you can still continue.
If you enter incorrect coordinates it will show an error.

**Coding plans:**

I kept it as modular as possible so that functions can be reused. 
Started with the default properties the rover and its environment should have like facing, position and grid bounds.
Then created functions that will split the input command into single commands.  Then I can determine what the input type is.
Created 2 main functions for moving and changing facing.  In testing I found that the facing function was not working correctly.  Once fixed the test passed.
Then added additional functions for checking if the rover is out of bounds and resetting it.

I used javascript and html as its where my strength lies and it keeps it from getting too uncomplicated.

**TESTING:**

I did manual positive and negative testing.  Ran the test command from the document first:
8 8
1 2 E
MMLMRMMRRMML
Expected result: 3 S S
Actual result: 3 S S
Passed.

Test moving:
2 2
0 0 N
M
Expected result: 0 1 N
Actual result: 0 1 N
Passed.

Test facing:
2 2
0 0 N
RRL
Expected result: 0 0 E
Actual result: 0 0 E
Passed

Test advanced facing:
2 2
0 0 N
LLL
Expected result: 0 0 S
Actual result:  0 0 E
Failed

Test advanced facing(after fix):
2 2
0 0 N
LLL
Expected result: 0 0 S
Actual result:  0 0 E
Passed.

Test out of bounds:
2 2
0 0 N
RMMM
Expected result: Game Over
Actual result: Game Over
Passed

Test incorrect input grid:
A 2
0 0 N
MMM
Expected result: Game Over
Actual result: Game Over
Passed

Test incorrect rover position:
2 2
A 0 N
MMM
Expected result: Game Over
Actual result: Game Over
Passed

Test incorrect rover instructions:
2 2
0 0 N
ab1
Expected result: 0 0 N (because the initial grid has been set but the commands will be ignored)
Actual result: 0 0 N
Passed







