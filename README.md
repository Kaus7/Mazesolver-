# Mazesolver-
The mazes that the program can solve are given in the form of text files. A file can contain a singular and symmetrical (square) mazes of a certain dimension. The maze is made 
up of integers from 0 to 9 as the path and * as barriers. The program can determine the number of paths found, the cheapest path, the cost of the cheapest path, and the 
shortest path. To begin the process, a maze file is opened. Then, the dimension of the maze is retrieved by determining the length of the first line in the file. Since the
mazes are square, this is the only dimension needed. Next, space is allocated for a double pointer with the dimension of the maze, and then the elements are filled with the 
contents of the maze to create an array-like pointer depiction of the maze file. This allows for the maze to processed.

The array is fed to a function that generates all the possible valid paths. This is done by depth first search, wherein the program will search as far as possible in one 
direction or branch of a maze until barriers obstruct all the possible moves except for backtracking. As a path is determined, the visited array cells are marked so that the 
path is visible in the event of backtracking. This analogous to the purpose of Hansel and Gretel’s trail of breadcrumbs. As a path is traversed, the path - a series of integers
from 0 to 9 - is stored in a pointer and is altered with the search process.

Once an exit is found, space is added to a double pointer containing all the paths generated for that maze and the current path string is copied in. Also, a variable is 
incremented that counts the number of individual paths found. Next, the shortest path is determined by comparing the string lengths of the paths in the paths double pointer. 
Then, the cheapest path is found by adding the series of integers that make up a given path within all the determined paths. The shortest path and cheapest path do not have to 
be the same path, since the integer path numbers vary, which is why both functions are necessary.
