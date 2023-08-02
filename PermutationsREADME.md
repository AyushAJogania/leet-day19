# leet-day19

# Permutations of Distinct Integers

This C++ program generates all possible permutations of distinct integers from an input array `nums`. It uses a backtracking algorithm to efficiently find all combinations.

## Problem Description

Given an array `nums` of distinct integers, we need to find all possible permutations of the integers in the array.

## Input

The input array `nums` is provided as a vector of integers.

## Output

The program will output a vector of vectors, where each inner vector represents a permutation of the integers in the input array.

## Algorithm

The program uses a backtracking algorithm to generate permutations. The basic idea is to consider each integer in the input array and recursively generate all permutations by swapping elements.

1. Create a result vector to store the permutations.
2. Create a current vector to store the current permutation being generated.
3. Create a boolean vector `used` to keep track of which integers have been used in the current permutation to avoid repetitions.
4. Start the `backtrack` function with an empty `current` vector and the `used` vector initialized to all `false`.
5. In the `backtrack` function:
   - If the size of the `current` vector is equal to the size of the input array `nums`, add the `current` vector to the `result` vector.
   - Otherwise, for each integer in `nums`, if it has not been used, add it to the `current` vector, mark it as used, and recursively call the `backtrack` function.
   - After the recursive call, remove the last integer from the `current` vector and mark it as unused to backtrack and consider other possibilities.
6. Return the `result` vector containing all the permutations.

## How to Use

1. Make sure you have a C++ compiler installed on your system.
2. Copy the provided C++ code into a file named `permutations.cpp`.
3. Compile the code using the following command:

   ```
   g++ permutations.cpp -o permutations
   ```

4. Run the executable:

   ```
   ./permutations
   ```

5. The program will generate all possible permutations of the integers in the input array and display the results.

## Example

Input:
```
nums = {1, 2, 3}
```

Output:
```
Permutations:
1 2 3 
1 3 2 
2 1 3 
2 3 1 
3 1 2 
3 2 1 
```

## Constraints

- The input array `nums` will have at most 6 elements.
- The integers in `nums` are distinct and in the range of -10 to 10.

## Time and Space Complexity

The time complexity of the algorithm is O(n!), where n is the size of the input array. This is because there are n! possible permutations to generate.

The space complexity is O(n), which represents the maximum depth of the recursive call stack.

