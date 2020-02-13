# Sudoku Solver

A simple Sudoku solver for any puzzle, regardless of difficulty. It is implemented using [NumPy](http://www.numpy.org/) arrays in Python 3.

You can view the [functions](https://nbviewer.jupyter.org/github/ThomasDelatte/SudokuSolver/blob/master/Sudoku/functions.ipynb) and the [sudoku](https://nbviewer.jupyter.org/github/ThomasDelatte/SudokuSolver/blob/master/Sudoku/sudoku.ipynb) notebooks on nbviewer.

## Features

The Sudoku solver uses a backtracing algorithm: it tries filling empty cells one by one. Whenever it finds that the current cell cannot lead to a viable solution, it removes it and backtracks to the previous cell.

It is better than a naïve, brute-force approach where we generate all possible combinations of digits in each cell, as it drops a set of permutations whenever it backtracks.

On [world's hardest Sudoku](http://www.telegraph.co.uk/news/science/science-news/9359579/Worlds-hardest-sudoku-can-you-crack-it.html) it takes about 5 seconds to solve. 800000000003600000070090200050007000000045700000100030001000068008500010090000400

On a standard Sudoku, it takes less than a second. 
000090010300010200000400067007500000006029081509000000200000000008000000160305002

## Installation and Usage

* Clone this repo to your computer.

* Install the requirements using `pip install -r requirements.txt`.
    * Make sure you use Python 3.
    * You may want to use a virtual environment for this.

* Edit the sudoku script and type in a Sudoku when asked to, in the requested format. For example:
    * 000090010300010200000400067007500000006029081509000000200000000008000000160305002

>[0--0--0--0--9--0--0--1--0]  
>[3--0--0--0--1--0--2--0--0]  
>[0--0--0--4--0--0--0--6--7]  
>[0--0--7--5--0--0--0--0--0]  
>[0--0--6--0--2--9--0--8--1]  
>[5--0--9--0--0--0--0--0--0]  
>[2--0--0--0--0--0--0--0--0]  
>[0--0--8--0--0--0--0--0--0]  
>[1--6--0--3--0--5--0--0--2]  

* Run the rest of the script. It will return the solution:

>[6--7--2--8--9--3--4--1--5]  
>[3--4--5--6--1--7--2--9--8]  
>[9--8--1--4--5--2--3--6--7]  
>[8--1--7--5--3--4--6--2--9]  
>[4--3--6--7--2--9--5--8--1]  
>[5--2--9--1--6--8--7--3--4]  
>[2--5--3--9--7--1--8--4--6]  
>[7--9--8--2--4--6--1--5--3]  
>[1--6--4--3--8--5--9--7--2] 


## License

See LICENSE for details of the GNU GPL v3.0 license that this software falls under.