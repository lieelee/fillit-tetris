# 𝌙 fillit

![2021-03-19 14 02 32](https://user-images.githubusercontent.com/52679439/111863021-22bc8c80-8916-11eb-89b8-917c42d4b541.gif)


**The allowed functions are: exit, open, close, write, read, malloc, free.**

## Goal

Fillit is a project that allows you to learn recursive programming: searching for the optimal solution among a huge set of possibilities. In this project, you will be tasked with developing an algorithm for assembling Tetriminos into the smallest possible square.
A Tetriminos is a four-block geometric design that many of you may be familiar with from the popular game Tetris. 


![Screen Shot 2021-03-02 at 12 23 00 AM](https://user-images.githubusercontent.com/52679439/109619422-9d4f7480-7aed-11eb-970c-9c9e65bc80d9.png)

## About this project 

A Tetrimino is made up of 4 characters(#) with the empty space represented by a dot(.) character. It is similar to the Tetris game, but in this project, the Tetrimino isn’t rotatable.

![Screen Shot 2022-05-07 at 11 58 40 PM](https://user-images.githubusercontent.com/104736314/167288604-2adbc159-41ff-4528-bce8-fa9c358c4f48.png)

**Input is passed into a program as a text file and has specific rules to be valid.**

1. Every Tetriminos description consists of 4 lines and each Tetriminos is separated by an empty line. 
2. Precisely 4 lines of 4 characters followed by a new line. 
3. Each character must be either a ‘#’ when the character is one of the 4 blocks of a Tetriminos or a ‘.’ if it’s empty. 
4. Each block of a Tetriminos must be in contact with at least one other block on any of its 4 sides.
5. Tetriminos occupy only 4 of 16 available boxes, it is possible to describe the same Tetrimino in multiple ways. However, the rotation of a Tetrimino    describes a different Tetrimino from the original in the case of this project.

In this project, my roles were to verify and validate if the input had passed, saved the data that is read from the text file to the right data structure, prevent all possible error cases from happening and to free all the memory that were dynamically used during run time at the end.
Each input was composed of 16 ‘.’ characters, 4 ‘#’ characters and new line characters at the end of each line. Additionally, It should be composed by the Tetriminoes blocks and the maximum blocks should be within 25. If it’s not validate input, It returns an error and ends. To verify if it was a valid block was one of the hardest challenges. After writing a bunch of simulations, I came up with the idea to count the total number of side touches. Valid Tetriminoes blocks have a total of 6 sides touching between each block. Then I had to decide which data structure I should use. I tried with a 3d array and failed many times. Then I switched to ‘node linked list’ because it is easy to add new elements dynamically. I read the text file with the previous project ‘get_next_file’ and saved each line of block to 2d array.

## Steps

1. Read an input file using a [get_next_line](https://github.com/lieelee/get_next_line). As It reads an input file, It saves the input Tetriminos into the string(char *tet) inside of the structure(t_tetris). 

![Screen Shot 2022-05-08 at 12 57 32 AM](https://user-images.githubusercontent.com/104736314/167288826-ec0c2e32-f2ad-4a75-85fc-3e7bfad92782.png)

2. Check the Input validation

<img width="1001" alt="Screen Shot 2022-05-08 at 12 24 43 AM" src="https://user-images.githubusercontent.com/104736314/167288838-f749d840-aafd-452d-8d01-5b0ff749d4d0.png">

Other than valid input rules above, there is one more thing to consider. It has to be a valid Tetriminos figure. I used the “Count Method” that is mentioned in [Beth Nenniger's blog post.](https://medium.com/@bethnenniger/fillit-solving-for-the-smallest-square-of-tetrominos-c6316004f909) ). A valid piece has either 6 or 8 adjacencies. 

3. Find the smallest square. 

Recursive backtracking method is utilized for the solution. 

In this project, my responsibilities included 
1. saving the data read from the text file to the correct data structure.
2. verifying and validating the input2. 
3. preventing all conceivable error scenarios
4. freeing any dynamically used memory at the end.
Each line included 16 '.' characters, four '#' characters, and a new line character at the end of each line. It should also be made up of Tetriminoes blocks, with a maximum of 25 possible combinations. It returns an error and terminates if the input is not validated. One of the most difficult tasks was determining whether or not the block was genuine. I decided to use the Count Method after creating a handful of simulations. Tetriminoes blocks that are valid have a total of either 6 or 8 sides that touch. After that, I had to choose which data structure to employ. I started with a 3d array and kept failing. Then I switched to a 'linked list,' which allows me to dynamically add new elements. 


