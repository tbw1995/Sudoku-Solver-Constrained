Disprove that this code generate valid n^2 x n^2 Sudoku Grids
-


I'm complete with my Sudoku Project and others have been skeptical that I can generate pre-filled valid Sudoku grids in poly-time. 

Now, disprove formally that this code won't print one out of n! valid grids sequentially of 9 x 9, 12 x 12, ..... ---- > n^2 x n^2


Remember, the rules for a *12 x 12*. it would be *3 x 4* squares. You'll have to know how a valid Sudoku grid would map out for a n x n. eg. *9 x 9* would be *3 x 3*.

A 9 x 9 grid would follow a list that has a length of non-repeating 9 elements.

You are asked for input to map out valid grid in O(n^3) time.

HINT: If you generate larger grids than 9 x 9, you'll need to make sure your input is given for human readability eg.**['[01]','[02]'...]**

    print('enter with [1,2,3...] brackets')
    tup = input()[1:-1].split(',')
    x = input('Enter mapping valid Sudoku eg. 3 for 9 x 9:')
    e = input('Enter 9 for 9 x 9 ...12 for 12 x 12:')
    f = input('Enter 3 if its a 9 x 9 ... n^2 x n^2:')
    x = int(x)
    e = int(e)
    f = int(f)
    squares = []
    for index in range(len(tup)):
      tup.append(tup.pop(0))
      squares.append(tup.copy())
    
        #Everything below here is just printing
    for s in range(x):
          for d in range(0,e,f):
            for si in range(s,e,f):
              for li in range(d,d+f):
                print(squares[si][li], end = '')
            print('')



If you can't disprove, then prove it. And, if it is non-finite subsets of n^2 x n^2 but with some sets not mappable then prove that as well.


Gratitude and Appreciation would be much given as an award.

I have a link to an improved code-https://codereview.stackexchange.com/a/221537/194047
