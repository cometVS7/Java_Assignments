# Assignment 04: Mathematical Vector Operations & Exception Handling

## Description
This project implements a **Vector** class capable of performing fundamental linear algebra operations in 2D and 3D space. It emphasizes **Data Integrity** and **Domain-Specific Error Handling** by restricting operations to compatible dimensions and ensuring mathematical correctness through custom Java exceptions.

## Key Features
- **Dimensional Validation:** Restricts vector creation to 2D or 3D space, throwing a `VectorException` for unsupported dimensions.
- **Linear Algebra Operations:** Implementation of core mathematical operations:
    - **Vector Addition:** Component-wise sum of two vectors.
    - **Vector Subtraction:** Component-wise difference between two vectors.
    - **Dot Product:** Calculates the scalar product, a critical operation in similarity measures and neural networks.
- **Custom Exception Handling:** Utilizes a user-defined `VectorException` to handle dimension mismatches and invalid initializations.
- **Input Robustness:** Employs `InputMismatchException` handling to ensure only numeric data is processed during vector population.


## Technical Specifications
### 1. Vector Class
- **Attributes:** Uses a private `double[]` array to store component values and an `int` for dimension.
- **Encapsulation:** Employs private helper methods like `checkDimensions()` to validate compatibility before performing operations.
- **Mathematical Logic:** Implements $V_1 \cdot V_2 = \sum_{i=1}^{n} a_i b_i$ for dot products and component-wise operations for addition/subtraction.

### 2. Error Handling Flow
- **Initialization:** Validates if $n \in \{2, 3\}$.
- **Operation Safety:** Checks if $dim(V_1) == dim(V_2)$ before execution.
- **User Input:** Catches non-numeric entries during console interaction.


## File Structure
- `Vector.java`: The blueprint class containing mathematical logic and dimension checks.
- `VectorException.java`: Custom exception class for handling vector-specific errors.
- `VectorMain.java`: The driver class for user interaction and operation execution.
