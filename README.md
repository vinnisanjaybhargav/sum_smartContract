// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract XYZ {
    // State variables
    uint public data;
    address public owner;

    // Constructor
    constructor() {
        owner = msg.sender;
        data = 0;
    }

    // Function to set data
    function setData(uint _data) public {
        require(msg.sender == owner, "Only the owner can set data");
        data = _data;
    }

    // Function to get data
    function getData() public view returns (uint) {
        return data;
    }
}
