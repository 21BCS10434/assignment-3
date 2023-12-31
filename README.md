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


License // SPDX-License-Identifier: MIT



https://www.loom.com/share/01d161196c034583b36798e1ca6b6fe0?sid=7b9a8ad4-c387-4f4e-9d97-e9937066c93e
