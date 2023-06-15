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

In the solidity compiler, make sure that the checkbox for auto compile is checked, and click "Compile



