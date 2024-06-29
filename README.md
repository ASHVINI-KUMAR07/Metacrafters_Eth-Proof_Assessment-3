PROJECT TITLE
write a smart contract that implements the require(), assert() and revert() statements.

DESCRIPTION
REQUIREMENTS:

There are four requirements for the project which we will explain in detail in the video:

You will submit your project on GitHub, so you will need an account and know how to share a public repository
You will include a README.md file in your project's GitHub repository (root folder). The README should provide a concise and clear overview of your project's purpose and functionality. This will help other developers understand the motivation behind your project and how to use it.
To assist you in creating your README, we have provided a starter template you can use.
This is an example of a README. Note that yours does not need to be this detailed. This is simply a reference.
You will record a video of 5 mins or less reviewing the three contracts you choose - Loom is a great tool to use if needed.
In the video, you will do a code walk-through where you share your screen and explain the code. In the video, explain the code and what it is doing.
Note: we will accept just audio with a screenshare, but, we highly recommend doing the video and screenshare since it will better prepare you for job interviews.
For some assessments/projects, you will need to share a transaction ID. (This project is NOT one of them so just type any number in the transaction ID box.)
Getting Started
ENVIRONMENT
This code we are running on the online Solidity IDE that is https://remix.ethereum.org/ here we'll perform the code. as we are on the remix website just by clicking on the start coding we'll able to do coding in Solidity.

EXECUTING PROGRAM
ETH+AVAX assesment code

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract DiabeticPatient {
    address public patient;
    uint256 public insulin_level;

    constructor() {
        patient = msg.sender;
    }

    function set_insulin(uint256 _insulin) public {
        require(_insulin < 25, "Higher level may cause Hypoglycemia");
        insulin_level = _insulin;
    }

    function check_insulin() public view {
        assert(patient ==msg.sender);
    }
    function modify_insulin_level() public {
        if(msg.sender != patient) {
            revert(" Only patient can change the INSULIN level according to the meal");
        }
        insulin_level=15;
    }
}


AUTHORS
Contributed by name : ASHVINI KUMAR Email ID : ashvinikumarcuchd123@gmail.com

GITHUB Link : [https://github.com/Ishi181/ETH-assesment/blob/main/README.md%20ETH](https://github.com/ASHVINI-KUMAR07/challenge3/tree/main)

Loom Video link :https://www.loom.com/share/9eb931dff8d843c9b45d6c06db07e306?sid=efcfe262-71d2-4f5c-a286-97f6ecc7316c

LICENSE
This project is licensed under the // SPDX-License-Identifier: MIT License - see the LICENSE.md file for details.
