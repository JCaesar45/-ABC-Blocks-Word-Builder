```markdown
# ABC Blocks Word Builder

## Overview
This project provides a function to determine whether a given word can be spelled using a collection of childhood alphabet blocks. Each block has two letters, and once a letter on a block is used, that block cannot be used again. The function is case-insensitive, making it flexible for various input formats.

## Collection of Blocks
The collection consists of 20 blocks, each with two distinct letters:

| Block | Letters |
|---------|---------|
| 1       | B, O   |
| 2       | X, K   |
| 3       | D, Q   |
| 4       | C, P   |
| 5       | N, A   |
| 6       | G, T   |
| 7       | R, E   |
| 8       | T, G   |
| 9       | Q, D   |
| 10      | F, S   |
| 11      | J, W   |
| 12      | H, U   |
| 13      | V, I   |
| 14      | A, N   |
| 15      | O, B   |
| 16      | E, R   |
| 17      | F, S   |
| 18      | L, Y   |
| 19      | P, C   |
| 20      | Z, M   |

*Note:* The complete alphabet is guaranteed among all sides of the blocks.

## Usage
The main function `canMakeWord(word)` takes a string input and returns a boolean indicating whether the word can be constructed from the available blocks.

### Example
```javascript
console.log(canMakeWord("bark"));    // true
console.log(canMakeWord("BooK"));    // false
console.log(canMakeWord("TReAT"));   // true
console.log(canMakeWord("COMMON"));  // false
console.log(canMakeWord("squAD"));   // true
console.log(canMakeWord("conFUSE")); // true
``

## Implementation Details
- The function converts the input word to uppercase to ensure case insensitivity.
- It iterates through each character in the word, attempting to find a matching block that hasn't been used yet.
- If a matching block is found, it marks that block as used.
- If any character cannot be matched with an unused block, the function returns `false`.
- If all characters are matched successfully, the function returns `true`.

## License
This project is for educational purposes and demonstrates basic logic for matching words with a set of constraints.
