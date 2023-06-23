# Token-Creation-Project
The purpose of this code is to create contracts and the following repository contains instructions on how to run the code in Remix Online IDE and the source code for the output.
## Getting Started
Copy the file below:

```Java
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public tokenName = "Sample";
    string public tokenAbbrv = "SMP";
    uint public totalSupply = 0;

    // mapping variable here
    mapping (address => uint) public balances;

    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn (address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}

```
## Executing the Program

To run this program, you must use Remix, an online IDE for developing, deploying, debugging, and testing Ethereum and EVM-compatible smart contracts. Head over to the Remix website at https://remix.ethereum.org/.

You should be redirected to the home page of the website. You should see the phrase "new file" highlighted in blue. Click it and enter your desired name for the file.

Once you have created the file, paste the code you copied earlier.

After pasting the file, look over to the left side of the website. You can see different icons, but I want you to hover your pointer and find "Solidity Compiler" and click on it.

In the solidity compiler, ensure the checkbox for auto compile is checked, and click the refresh icon named "Compile(your file name)."

Next, hover your pointer over the icon below and click "Deploy and run transactions."

Here, you can experiment with the number of tokens minted and burned. For starters, click the yellow button named "Deploy," which should officially create the token that is ready to be minted and burned.

Under the deployed contracts tab, click the following buttons to view the token name, abbreviation, and of course, the total supply you currently have. 

Now, if you want to experiment with the minting and burning function, scroll to the very top, and you should see "Account" from there, you can choose what accounts you would like to transact with, but to make things easier, you can start with the default one. Copy the account details.

After copying the details, go to the "Deployed Contracts" tab page, and you should be able to see the buttons named "burn" and "mint." Click the arrow down beside them, and there will be text fields displayed as "_address."
and "_value." In the address text field, paste the copied account details from earlier, and in the value text field, input the number of tokens you would like to mint and burn.

Once you are done, click the "tokenSupply" button again to view the updated amount of tokens you have.

Do note that no transaction or error will happen if the token you burned exceeds the one you minted.




