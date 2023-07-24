# assignment-3

EvenOrOdd Smart Contract
This is a simple Ethereum smart contract written in Solidity to check whether a given number is even or odd. The contract contains a single function checkEvenOrOdd that takes an unsigned integer as input and returns a string indicating whether the number is even or odd.

Function
checkEvenOrOdd(uint256 _number) external pure returns (string memory)
This function takes a positive integer _number as input and returns a string "Even" if the number is even, "Odd" if the number is odd, and reverts with an error message "Invalid number" if the number is negative.

The function uses the following control flow statements for validation:

.require: Ensures that the input number is positive. If _number is less than or equal to 0, the function will revert with the error message "Number must be positive."

.assert: Checks whether the _number is less than or equal to type(uint256).max / 2 + 1. This is done to avoid arithmetic overflow when calculating the remainder of the division by 2. If the condition is not met, the function will revert due to the assert statement.

.If the _number passes both validations, it will calculate the remainder of the division by 2. If the remainder is 0, the function returns "Even"; if the remainder is 1, the function returns "Odd." If for some reason the remainder is neither 0 nor 1, the function will revert with the error message "Invalid number."

Usage
To use this smart contract, you can deploy it to the Ethereum blockchain using a development environment like Remix or Truffle. Once deployed, you can interact with the contract by calling the checkEvenOrOdd function with the desired number as an argument.
Ensure that you have sufficient gas to execute the transaction, especially if the number is close to the maximum value for a uint256

Disclaimer
This smart contract is provided as-is, and no guarantees are made about its security or functionality. It is essential to review and audit the code thoroughly before using it in production environments

License // SPDX-License-Identifier: MIT


https://www.loom.com/share/e093b6b65ab2477ba6f09dd2d61041b3?sid=2fd7c505-a30b-4b24-88f9-c3469e62c0eb
