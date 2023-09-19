# CTO

This Solidity smart contract works as a simple mint and burn smart contract in order to test certain functions in solidity.

## Description


This Solidity smart contract simply simulates the mint and burn function in a blockchain where
the custom token "CATTO" will be utilized.


## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

```javascript

pragma solidity 0.8.21;

contract MyToken {

    // public variables here

    string public Token_Name = "CATTO";
    string public Token_abv = "CTO";
    string warn = "insufficient tokens";
    uint public Supply = 0;
	

    // mapping variable here

    mapping(address => uint) public balances;


    // mint function


    function mint (address _address, uint _value)public{

	
   	Supply += _value;
	balances[_address] += _value;


    }
    // burn function
    
   function burn (address _address, uint _value)public{

       
      if(balances[_address] >= _value){
	
	      Supply -= _value;
	      balances[_address] -= _value;

	   }
	


   }



}


```

To compile the code, simply press ctrl + s and once the compilation is finished, click on the Ethereum icon on the leftmost side of the remix website right above the bug icon, and click on the orange "Deploy" button and then below it, the Deployed Contracts should be filled out
and press on it and the functions should appear.

## Authors

Metacrafter Kyle  
