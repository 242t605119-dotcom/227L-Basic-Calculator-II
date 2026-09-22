# LeetCode 227 - Basic Calculator II

## Problem

Given a string `s` representing a valid expression, implement a basic calculator to evaluate it.

The expression contains:

* Non-negative integers
* `+`
* `-`
* `*`
* `/`
* Spaces

Division should truncate toward zero.

## Example

### Input

```text
s = "3+2*2"
```

### Output

```text
7
```

### Example 2

```text
s = " 3/2 "
```

Output:

```text
1
```

### Example 3

```text
s = " 3+5 / 2 "
```

Output:

```text
5
```

## Approach

Use a stack to handle multiplication and division before calculating the final sum.

For each number:

* `+` → add the number to the stack.
* `-` → add the negative number to the stack.
* `*` → multiply the top stack value by the current number.
* `/` → divide the top stack value by the current number.

At the end, the sum of all stack values gives the answer.

## Algorithm

1. Initialize an empty stack.
2. Traverse the expression character by character.
3. Build the current number.
4. When an operator is found, process the previous number using the previous operator.
5. Store addition and subtraction values directly in the stack.
6. Immediately calculate multiplication and division.
7. Return the sum of the stack.

## Complexity

* Time Complexity: `O(n)`
* Space Complexity: `O(n)`

Where `n` is the length of the expression.

## Language

Python

## LeetCode

Problem: 227 - Basic Calculator II

## Author

**T.Nandhini**
