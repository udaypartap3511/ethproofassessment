# making token

this solidity program is to make a simple token that demonstrate how to make and use tokens.

## DESCRIPTION

this program is a contract for making tokens, solidity is the programming language use for developing smart contracts on the ethereum blockchain. the contract some variables that have information about the tokens, mapping is used for  holding the no. of tokens, mint fuction for adding tokens,burn function for deleting tokens.

## Getting Started

### Executing program

to run this program, you can remix, an online solidity IDE. Let's start with remix website https://remix.ethereum.org/.

On remix website , create a new file option and use .sol extension for file (ex. ethproof.sol) on left-hand bar. copy and paste code into the file:

```javascript

// SPDX-License-Identifier: MIT
pragma solidity 0.8.26;

/*
       REQUIREMENTS
    1. Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
    2. Your contract will have a mapping of addresses to balances (address => uint)
    3. You will have a mint function that takes two parameters: an address and a value. 
       The function then increases the total supply by that number and increases the balance 
       of the “sender” address by that amount
    4. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. 
       It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
       and from the balance of the “sender”.
    5. Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal 
       to the amount that is supposed to be burned.
*/

contract MyToken {

    // public variables here
    string public tokenname = "Uday Partap Singh";
    string public tokenabbrev = "UPS";
    uint public totalsupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;
    // mint function
    function mint(address _address, uint _value) public 
    {
        totalsupply += _value;
        balances[_address] += _value;
    }
    // burn function
    function burn (address _address,uint _value) public 
    {
        if (balances[_address] >=_value)
        {
            totalsupply -= _value;
            balances[_address] -= _value;
        }
        
    }
}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.26" (or another compatible version), and then click on the "Compile ethproof.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with balance and also with mint and burn function. Click on the "MyToken" contract in the left-hand sidebar, and then click on the "mint" and "burn" function. Finally, click on the "transact" button .

## Authors

upartap12@gmail.com


