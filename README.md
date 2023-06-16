# ETHAssessment_Garcia

## Creating a token in ETH 

Through the creation and execution of token transactions on Ethereum, this solidity program's simple token generator uses Solidity's fundamental features. This project aims to assist users in comprehending the functionality of executing a program in Solidity and demonstrating how it operates. 

## Description 

It uses Solidity's fundamental features to demonstrate how it generates or allocates tokens to accounts. Moreover, Ethereum uses Solidity's computer language to create smart contracts or programs kept on a blockchain. This program has functions that may be customized at the user's expense, allowing them to create token values and add and subtract them. The program will give a general understanding of how the Solidity programming language interacts with the Ethereum Blockchain. 

## Getting Started 

### Where to Access 
To run this program you may use REmix, which is an online Solidity IDE. To get starte and use the code provided, go to Remix website at https://remix.ethereum.org/.

### Executing the Program 
Once you are inside the IDE, click on the "+" buttong on the left-hand sidebar to create a new file inside the existing workspace, or create a new workspace for yourself depending on how you want to use it. After, save the file woth .sol extension at the end. (e.g. YouAreTheBest.sol).

```javascript
pragma solidity 0.8.18;
contract MyToken {

    // public variables here
    string public tokenName = "Adam";
    string public tokenAbbrv = "dam";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public remmy;

    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        remmy[_address] += _value;
    }

    // burn function
    function burn (address _address ,uint _value) public {
        if (remmy[_address] >= _value) {
        totalSupply -= _value;
        remmy[_address] -= _value;
    }
  }
}

```

To compile the code, Click on the "Solidity Complier" Tab in the left-hand sidebar. Make sure the "Compiler" options is set to "0.8.18" (or another compatible version), and then click on the "Complie myToken.sol button

After a successful compilation, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar just below the Solidity Compiler tab. Select the "myToken" contract from the dropdown menu, and then click on the "Deploy" button.

From there, you will be able to see the contract deployed and be able to transact values from the mint function (used for adding tokens) , burn function (used for subtracting the amount of tokens inside the address , and the remainder function (displays the current deposited amount of your tokens)

## Authors 
Contributors names and contact infor
Adam Garcia aulricgarcia01@gmail.com 

## License

This project is licensed under the MIT License - see the LICENSE.md file for details

