# Sparse Matrix-Vector Multiplication (SpMV)
This repository contains an implementation of sparse matrix-vector multiplication (SpMV) using the Compressed Sparse Row (CSR) format. The program reads a sparse matrix in Matrix Market (MTX) format, converts it from Coordinate (COO) format to CSR format, and performs matrix-vector multiplication.

## Features
### Sparse Matrix Handling:

Reads matrices in Matrix Market format using mmio.c utilities.
Converts sparse matrices from Coordinate (COO) format to Compressed Sparse Row (CSR).
Handles large matrices efficiently with an O(N) conversion algorithm.

### Matrix-Vector Operations:

Performs matrix-vector multiplication using the CSR representation.
Outputs the results in a Matrix Market-like format.

### Input/Output:

Reads matrix files (A.mtx) and vector files (x.mtx).
Outputs result to a specified file (result.mtx).
File Overview
main.c - The main entry point, handling file reading, conversion, computation, and output storage.
main.h - Header file defining function prototypes.
mmio.c / mmio.h - Matrix Market I/O utilities for reading/writing MTX files.
Makefile - Build system configuration to compile the project using gcc with -std=c11.
### Test Cases:
Provided test matrices and vectors in test1/ and test2/ directories.

## Usage
#### To compile the program, run:
make

#### To execute the program:
./spmv <matrix_file> <vector_file> <result_file>

#### Example:
./spmv A.mtx x.mtx result.mtx

## Notes
Ensure that input files are in the correct Matrix Market format.
Results may have minor floating-point differences but should match the reference solution closely.
The program is optimized to avoid sorting operations and should perform efficiently even with large matrices.

## License
This project is for educational purposes.

