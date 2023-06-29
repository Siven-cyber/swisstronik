# swisstronik

Swisstronik Early Bird program
First 100 selected applicants

Tutorial: https://www.tiktok.com/@airdropsultan.id/video/7247749157828431109

Deploy Contract di http://remix.ethereum.org dengan menggunakan command di bawah.

task dan detail cek disini :
https://urlis.net/i98t8d1j

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract Register {
    string public github;
    address public owner;
    
    struct Referral {
        address referralAddress;
        string referralString;
    }
    
    Referral[] public referrals;
    
    constructor() {
        github = "ganti_pake_username_github_kalian";
        owner = “ganti_pake_address_kalian”;
    }
    
    function addReferral(address _referralAddress, string memory _referralString) external {
        require(msg.sender == owner, "Only the owner can add referrals.");
        referrals.push(Referral(_referralAddress, _referralString));
    }
    
    function totalReferrals() public view returns (uint256) {
        return referrals.length;
    }
}
