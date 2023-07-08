# Solidity Beginner

This is a sample solidity code to create a token. You can use this is a reference to create your own token with a name and symbol.You can also use functions to implement different functionalities like mint and burn.

## Description

In this project, I have created a token called Sangamesh and abbreviation - SY .Using our token, we can mint and burn to add or remove tokens from the balance. We can also check the balance of any address that we enter in balances.

## Getting Started

### Installing the code

You can run the code on remix or download it locally on your computer.

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:

```javascript
pragma solidity ^0.8.9;

contract MyToken {

    string public tokenName = "Sangamesh";
    string public tokenAbbreviation = "SY";
    uint public totalSupply = 100;
    mapping(address=>uint) public balances;

    function mint (address to_address, uint value) public{
        totalSupply += value;
        balances[to_address] += value;

    }
     function burn (address to_address, uint value) public{
         if (balances[to_address]>=value) {
        totalSupply -= value;
        balances[to_address] -= value;
        }
     }
}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.9" (or another compatible version), and then click on the "Compile MyToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it .
## Authors

Sangamesh Y

@sangamessshhh@gmail.com

## License

This project is licensed under the [MIT] License - see the LICENSE.md file for details
