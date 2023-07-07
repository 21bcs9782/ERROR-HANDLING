# ERROR-HANDLING

This is a Solidity smart contract that demonstrates different error handling techniques using `assert`, `revert`, and `require` functions.

## License

This contract is using the MIT License.

## Prerequisites

- Solidity ^0.8.17

## Contract Details

The `ErrorHandling` contract provides the following functions:

### `assertStatement(uint a,uint b)`

 {
    function assertStatement(uint a, uint b) public pure returns (uint) {
        // `assert` checks for conditions that should never be possible.
        // If the condition evaluates to false, it indicates a bug in the code,
        // and the transaction is reverted.
        assert(a != 0 && b != 0);
        
        uint result = a / b;
        return result;
    }


- This function demonstrates the usage of the `assert` function.
- It takes ‘a and b` parameter and checks if it is not equal to zero using the `assert` statement.
- If the condition fails, it triggers an "Internal error" and aborts the execution.

### `revertStatement(uint a,uint b)’

function revertStatement(uint256 a, uint256 b) public pure returns (uint) {
        // `revert` is used to explicitly revert the transaction execution,
        // typically due to invalid conditions or invalid inputs.
        if (a == 0 || b == 0) {
            revert("Cannot divide by zero.");
        }
        
        uint result = a / b;
        return result;
    }
    
  

- This function demonstrates the usage of the `revert` function.
- It takes `a` and `b` parameters and performs logical OR operation.
- If the `a and b` both are zero, it reverts the transaction with a custom error message stating that the “can’t divide by zero.”
- If the condition is met, it returns the result of the division of a and b.

### `requireStatement(uint a,uint b)`

function requireStatement(uint a, uint b) external pure returns (uint) {
        // `require` is used to validate inputs or conditions, and if they
        // evaluate to false, the transaction is reverted.
        require(a != 0 && b != 0, "Inputs must be non-zero.");
        
        uint result = a / b;
        return result;
    }
}

- This function demonstrates the usage of the `require` function.
- It takes an `a and b` parameter and performs logical AND operation.
- It first checks if `a and b` is not equal to zero using the `require` statement.
- If the condition fails, it reverts the transaction with a custom error message stating that theinputs must be non zero.
- If the condition is met, it returns the result of the a/b.

## Usage

1. Make sure you have Solidity ^0.8.17 installed.
2. Compile and deploy the `ErrorHandling` contract to a supported Ethereum network.
3. Interact with the deployed contract by calling the available functions and providing the required parameters.

##Authors
Sonia Beniwal
Mail id: 21BCS9782@gmail.com



