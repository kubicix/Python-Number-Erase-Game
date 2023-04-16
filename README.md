# Python-Number-Erase-Game
This is a Python function that implements a game called "Number Erase". The game is played on a board of random numbers, and the player can select a number on the board. If the number has two or more adjacent numbers of the same value, then all of those adjacent numbers are erased from the board, and the player earns points based on the value of the erased numbers and the number of erased numbers. The function takes two arguments: the number of rows and columns in the game board.

The function starts by defining two nested functions: fibonacci() and komsu_kontrol(). fibonacci() is a recursive function that calculates the nth number in the Fibonacci sequence. komsu_kontrol() is the most important function in the program. It takes four arguments: the row and column of the selected number, the value of the selected number, and a counter variable to keep track of the number of erased numbers. komsu_kontrol() first sets the value of the selected number to -1 to mark it as erased, then it checks the four adjacent numbers (up, down, left, right) to see if they have the same value. If an adjacent number has the same value, then komsu_kontrol() is called recursively on that number. After all adjacent numbers have been checked, komsu_kontrol() checks each column to see if all of its numbers have been erased. If so, it shifts all the numbers above the column down by one, and sets the rightmost number in the column to -1. komsu_kontrol() then returns the counter variable, which gives the number of erased numbers in the connected group.

The main part of the function starts by creating a random game board of the specified size and writing it to a file named "girdi.txt". It then enters a loop where the player selects a number from the board. If the selected number is out of bounds or has already been erased, then the loop continues. Otherwise, komsu_kontrol() is called on the selected number to erase any adjacent numbers with the same value. If there are fewer than two erased numbers, then the loop continues. Otherwise, the function calculates the points earned from the erased numbers using the fibonacci() function, adds them to the player's score, and prints the updated score. The function then shifts the numbers above the erased group down and writes the updated board to a file named "cikti.txt". The loop then repeats with the updated board until no more numbers can be erased.

![s1](https://user-images.githubusercontent.com/96316375/232332244-95006ee2-4e04-4eb6-9836-c03c1b8d5775.png)
![s2](https://user-images.githubusercontent.com/96316375/232332246-c4a2ba29-fdb1-4a44-9d91-150786ec6546.png)