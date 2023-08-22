## ETH AVX PROOF
## Require(),Revert() Assert() 
 The require(), assert(), and revert() statements are implemented in this Solidity project's smart contract.

## Description
The require(), assert(), and revert() statements are implemented in this Solidity project's smart contract.

1. Prior to execution, require is used to validate inputs and conditions.

2. Code that should never be false is checked using assert. Assertion failure most likely indicates a problem.

3. Use reverse() to cancel operations and undo state changes.
## Getting Started

### Executing program

Use the online Solidity IDE Remix to run this programme. Visit the Remix website at https://remix.ethereum.org to get started.

When you are on the Remix website, click the "+" icon in the left sidebar to start a new file. Put a.sol extension to the file, such as HelloWorld.sol. The code below should be copied and pasted into the file:

```pragma solidity ^0.8.13;

contract Error {
    function testRequire(uint _i) public pure {
 
        require(_i >= 10 && _i <= 100 , "Input must be between 10 to 100");
    }

    function testRevert(uint _i) public pure {

        if (_i <= 10 && _i>=100) {
            revert("Input must be greater than 10 msg by revert");
        }
    }

    uint public num;

    function testAssert() public view {
       
        assert(num != 0);
    }

   
}


```
Click the "Solidity Compiler" tab in the left-hand sidebar to compile the code. Click the "Compile Error.sol" button after making sure the "Compiler" option is selected to "0.8.4" (or another compatible version).

Using the "Deploy & Run Transactions" tab in the left-hand sidebar, you can deploy the contract after the code has been compiled. Click the "Deploy" button after selecting the "Error" contract from the drop-down menu.

You can communicate with the contract after it has been deployed by invoking the function. The variable and function names that are highlighted in the left sidebar should be clicked. To complete the function and retrieve the values and message, click the "transact" button.
