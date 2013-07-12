# Print number sequence as a spiral

Write a program in Ruby that takes one command line argument (referred to going forward as n). If n is not a perfect square print an appropriate error message and exit. If n is a perfect square then create a sequence from 1 to n and build a matrix from the sequence by walking in counter-clockwise spiral order. Once you have built the matrix print it, ensuring even column widths as in examples below and then exit.

Input:  1
Output: 1
       
Input:  2 is invalid, Please enter perfect square number
Input:  3 is invalid, Please enter perfect square number
Input:  4
Output: 4 3
        1 2
       
Input:  5 is invalid, Please enter perfect square number
Input:  9
Output: 9 8 7
        2 1 6
        3 4 5
       
Input:  16
Output: 16 15 14 13
         5  4  3 12
         6  1  2 11
         7  8  9 10
       
Input:  36
Output: 36 35 34 33 32 31
        17 16 15 14 13 30
        18  5  4  3 12 29
        19  6  1  2 11 28
        20  7  8  9 10 27
        21 22 23 24 25 26
       
Input:  64
Output: 64 63 62 61 60 59 58 57
        37 36 35 34 33 32 31 56
        38 17 16 15 14 13 30 55
        39 18  5  4  3 12 29 54
        40 19  6  1  2 11 28 53
        41 20  7  8  9 10 27 52
        42 21 22 23 24 25 26 51
        43 44 45 46 47 48 49 50
       
Work done!


# Running
    
    ./is.rb 1 2 3 4 5 9 16 36 64

