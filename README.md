# Solidity Assessment

This is the code for my Solidity Assessment for Metacrafters

### Executing program
These are the codes for initializing and declaring of variables
*
```
 // public variables here
    string public tokenName = "Pelep";
    string public tokenAbbrv = "PJ";
    uint public totalSupply = 0;


    // mapping variable here
    mapping (address => uint) public balances;
```

These are the code for the Mint and Burn function

```
  // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }


    // burn function
    function burn (address _address, uint _value) public  {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }```

#

