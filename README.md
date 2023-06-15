# Token-Creation-Project
The following repository contains instructions on how to run the code in Remix Online IDE and the source code for the output.
# Getting Started
Copy the file below:

```Java
pragma solidity 0.8.18;
contract MyToken {

    // public variables here
    string public tokenName = "Metal Gear Solid";
    string public tokenAbbrv = "MGS";
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
# Executing the Program
To run this program, you will have to use Remix, an online IDE for developing, deploying, debugging, and testing Ethereum and EVM-compatible smart contracts. Head over to the Remix website at https://remix.ethereum.org/.

You should be redirected to the home page of the website. You should be able to see the phrase "new file" highlighted in blue. Click it and enter your desired name for the file.

Once you have created the file, paste the code you copied earlier.

After pasting the file, look over to the left side of the website. You will be able to see different icons but I want you to hover your pointer and find "Solidity Compiler" and click on it.

In the solidity compiler, make sure that the checkbox for auto compile is checked, and click the button with the refresh icon named "Compile(your file name)".

Next, just hover your pointer over the icon below and click "Deploy and run transactions".

In here, you are free to experiment with the number of tokens minted and burned. For starters, click the yellow button named "Deploy" which should officially create the token that is ready to be minted and burned.

Under, the deployed contracts tab, click the following buttons to view the token name and abbreviation, and of course, the total supply that you currently have. 

Now, if you want to experiment with the minting and burning function, scroll to the very top and you should see "Account", from there you can choose what accounts would you like to transact with but to make things easier, you can start with the default one. Copy the account details.

After copying the details, go to the "Deployed Contracts" tab page and you should be able to see the buttons named "burn" and "mint". Click the arrow down beside them and there will be text fields displayed as "_address"
and "_value". In the address text field, simply paste the copied account details from earlier, and in the value text field, input the number of tokens you would like to mint and burn.

Once you are done. simply click again the "tokenSupply"  button to view the updated amount of tokens you have.

Do note that, no transaction or error will happen if the token that you burned is greater than the token you minted.




