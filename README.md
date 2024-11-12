// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract SimpleStorage {
    
    uint public storedValue;
    
    // Declare the event to track changes in the stored value
    event ValueChanged(uint newValue);

    // Function to set a new value and emit the ValueChanged event
    function setValue(uint _value) public {
        storedValue = _value;  // Store the new value
        emit ValueChanged(_value);  // Emit the event with the new value
    }

    // Function to retrieve the stored value
    function getValue() public view returns (uint) {
        return storedValue;
    }
}

