# Hilbert R-Tree

Current implementation supports 2D coordinates, but can be easily extended to support multidimensional coordinates as required.

The tree is built upwards from the bottom. The leaf nodes represent the actual 2D data points.\
An internal (non-leaf) node is represented by the Minimum Bounded Rectangle (MBR) of all its contained points.\
Each 2D point is represented as (x, y) and each rectangle is represented by its bottom-left and top-right points.

## Before Executing the code

1. Input file should contain the data in the following format (check Dataset.txt for example).

    - Each line contains one pair of coordinates (one point on the 2D plane).
    - The x and y coordinates should be separated by space.

2. Set the filename variable in function `main` in `tree.c` to either the relative path of \
the input file or its absolute path.

3. By default, the constructed tree is traversed in pre-order. To search for all the points contained within a rectangle, uncomment the code in function `main` and edit the rectangle's coordinates.\
`qmin` is the bottom-left coordinate
`qmax` is the top-right coordinate

## Executing the code

1. Navigate to the root directory of the project
2. Compile: Run `gcc tree.c`
3. Execute: Run `./a.out`. To print into an output file, run `./a.out > output.txt`
4. Compile and execute: `gcc tree.c && ./a.out`