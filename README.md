# ERC721-Burnable-NFT
ERC721 Burnable NFT
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

import "@openzeppelin/contracts/token/ERC721/extensions/ERC721Burnable.sol";

contract BurnNFT is ERC721Burnable {
    uint256 public nextId;

    constructor() ERC721("BurnNFT", "BNFT") {}

    function mint() public {
        _mint(msg.sender, nextId++);
    }
}
