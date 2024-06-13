# Transactions Under Solidity

This Solidity program is a simple "Transactions Under Solidity" program that demonstrates the basic syntax and functionality of the Solidity programming language. The purpose of this program is to serve as a starting point for those who are new to Solidity and want to get a feel for how it works.

## Description

This project is under solidity which includes a contract which have token, its abbreviation and its address and the no. of tokens we are going to add this will be transacted and will be updated in the balance and it also contains a condition that the transaction will not be executed if the no. of tokens to be burnt will be more than the no. of tokens minted. 

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., Transactions.sol). Copy and paste the following code into the file:

```Solidity
pragma solidity 0.8.18;
contract MyToken {

    // public variables here
    string public tokenName= "Aman Bansal";
    string public tokenAbbrev="AB";
    uint public TotalSupply= 0;

    // mapping variable here
    mapping(address=>uint) public balances;


    // mint function
    function mint(address _address, uint _value) public {
        TotalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn (address _address, uint _value) public {
        if(balances[_address]>= _value){
            TotalSupply -= _value;
            balances[_address] -= _value;
        }
    }


}

```
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Transactions.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "Transactions" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the sayHello function. Click on the "Transactions" contract in the left-hand sidebar, and then click on the function. Finally, click on the "transact" button to execute the function and retrieve the amount.

## Authors

Aman Bansal


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
