
# Pattern Matching with Z-Array and LPS'-Array

This code repository contains Python scripts for performing pattern matching using the Z-array and LPS'-array algorithms. It consists of two main parts:

## Part 1: `calculate_z_array` and `find_pattern_positions`

### `calculate_z_array(s)`

This function computes the Z-array for a given string `s`. The Z-array is an array where each element `z[i]` represents the length of the longest substring that is also a prefix of the string, starting from position `i`. The function returns the Z-array.

### `find_pattern_positions(t, p)`

This function finds all positions in string `t` where pattern `p` is present using the Z-array. It concatenates the pattern `p` and the text `t` with a special character `$` in between, computes the Z-array of the concatenated string, and then identifies positions where the Z-array value is equal to the length of the pattern `p`. It returns a list of positions where the pattern is found in the text.

## Part 2: `compute_lpsP_from_z`

### `compute_lpsP_from_z(z)`

This function computes the LPS'-array from a given Z-array `z`. The LPS'-array is defined as the length of the longest nontrivial suffix of a string `P[1..i]` that matches a prefix of `P` such that `P[lps[i] + 1]` is not equal to `P[i + 1]`. If those two characters are equal, `lps'[i]` is set to 0. The function returns the LPS'-array.

## Usage

To use the provided functions for pattern matching, follow these steps:

1. Import the functions into your Python script.
2. Call `calculate_z_array(s)` to compute the Z-array for a given string `s`.
3. Call `find_pattern_positions(t, p)` to find all positions of pattern `p` in text `t` using the Z-array.
4. Call `compute_lpsP_from_z(z)` to compute the LPS'-array from a given Z-array `z`.

## Sample Input Files

The code is designed to process multiple input files. Each input file should contain two lines: the first line contains the text `t`, and the second line contains the pattern `p`. The code reads these input files, performs pattern matching, and outputs the positions where the pattern is found in the text to separate output files.

## Output

The output is a series of output files (e.g., `sol_0.txt`, `sol_1.txt`) containing the positions where the pattern was found in the text.

