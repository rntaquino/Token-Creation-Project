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
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

