# RockPaperScissors

Group Members:
Aysu Sözen 
Ceyda Alpay @ceydalpay

Project Summary & Implementation Details:
In this program, we have two processes, parent and child processes. Child and parent processes select a
random numbers 1 to 3, which represent paper, rock or scissors item. Then two processes compare their
item and they increment their scores. First one, that reaches the score 5, wins the game. There are three
options for each round: child process can win, parent process can win or there can be a tie. And there are
two options for each game: child process can wi n or parent process can win.
In this project we use pipe mechanism as IPC. We first create pipe, then we use fork( fork() to create child and
parent processes. First, child selects a random number and convert number to corresponding paper, rock or
scissors item. We use pipe(0) for reading the item, so we close it first, and then we increment size by 1 for
not getting an arr ay out of bounds error. First item has written in pipe(1) and then it is closed. In parent
process, first process selects a random number and convert number to corresponding paper, rock or scissors
item, and then pipe(1) has closed and process allocate a s ize depends on the item that it chose. Then
pipe(0) has read and it is closed. We use while loop for the winning condition of game. If one of the process
gets 5 score, the game is over and processes are terminating.
