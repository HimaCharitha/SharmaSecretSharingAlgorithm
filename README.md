#Shamir's Secret Sharing Algorithm in C

##Overview
This program is a C implementation of a simplified version of Shamir's Secret Sharing Algorithm. The algorithm works by breaking up a secret into multiple shares (points) such that only a subset of those shares (of size k or more) can reconstruct the secret. The program reads multiple test cases and attempts to find the secret constant term c using the provided points. It also checks whether the given points are valid and determines if any of them are incorrect.

##Features
Polynomial-based secret sharing: Finds the constant term c (the secret) from multiple points.
Point validation: Checks if any points provided are invalid or incorrect based on the reconstructed polynomial.
Base conversion: Handles values in different numerical bases (e.g., decimal, binary, hexadecimal).

##Prerequisites
A C compiler such as GCC
Basic knowledge of polynomial functions and matrix operations (Gaussian Elimination is used here for solving systems of equations).

##Program Structure
Test Cases: Each test case consists of a set of points represented by coordinates in different numerical bases.
Polynomial Reconstruction: Given the points, the program reconstructs the polynomial and extracts the constant term c (which is the secret).
Error Checking: Identifies any incorrect points that do not fit the reconstructed polynomial.

##Input Format
The program works with test cases hardcoded in the main() function. Each test case consists of:
n: Total number of points (some of which may be incorrect).
k: Minimum number of correct points required to find the secret.
Points in various bases.

##Output Format
For each test case:
The constant term (the secret c) is printed.
If n > k, it prints any "wrong points" that do not lie on the polynomial curve. If there are no incorrect points, it prints "None."

##Functions:
decode_value(): Decodes a string value based on its base (e.g., binary, decimal, hexadecimal).
gaussian_elimination(): Solves a system of linear equations using Gaussian elimination.
find_constant_term(): Reconstructs the polynomial and returns the constant term c.
is_point_on_curve(): Checks whether a given point lies on the reconstructed polynomial curve.
solve_test_case(): Handles each test case, finding the secret and identifying incorrect points.
Future Improvements
Support for reading test cases dynamically from input files.
Enhanced error handling for incorrect or missing data.
Support for larger and more complex datasets.

##License
This project is open-source and can be freely modified and distributed.
