# Lesson 2 - Building HelloWorld.sol in Remix
## Coding HelloWorld.sol
* Solidity philosophy
* OOP basics of Solidity
* Contract Structure
  * SPDX License Identifier
  * Pragmas
  * Imports
  * Comments
  * Contract definition
* Variables
* Storage areas
  * Account storage
  * Memory
  * Stack
* Constructor function
* Functions
* Visibility
* Typing
* Return values

## Detailed contract structure
* (Review) Contract structure
* (Review) Variables
* (Review) Storage
* What are interfaces
* What are contracts, indeed
* Multiple objects per file
### References
https://docs.soliditylang.org/en/latest/grammar.html

https://docs.soliditylang.org/en/latest/structure-of-a-contract.html

### Code Reference
<pre><code>// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.7.0 <0.9.0;

interface HelloWorldInterface {
    function helloWorld() external view returns (string memory);
    function setText(string memory newText) external;
}

contract HelloWorld is HelloWorldInterface {
    string private text;

    constructor() {
        text = "Hello World";
    }

    function helloWorld() public view override returns (string memory)  {
        return text;
    }

    function setText(string memory newText) public override {
        text = newText;
    }
}</code></pre>

## Contract interaction
### Part 1
* Contract interactions using Remix
* Viewing state changes through functions
### Part 2
* State changing calls
### Part 3
* Payable functions
* Experimenting with payable calls

## Clean code and documentation
* (Review) Readability and standardization
* The Style guide
* Using the Linter
* Function order
* Layout
* Naming conventions
* Documentation
* NatSpec Format

### References
https://docs.soliditylang.org/en/latest/natspec-format.html#natspec

# Homework
* Create Github Issues with your questions about this lesson
* Read the references