# The Compendium
This initiative serves to break out every single solidity vulnerability that has thus far been identified, codify / categorize them, and then present the information into a detailed and concise source of knowledge for the solidity developer and auditor community.

This initiative will be documented live on my twitter: https://twitter.com/theweb3hacker

If you're interested in a high-quality smart contract audit at a resonable budget please feel free to reach out via twitter as well. If my team and I have a slot, we will do out best to accomodate!

Day | Topic | Overview
--- | --- | ---
**1** | [Transaction Order Dependence](/days/day1.md) | **NOTE:** Ethereum is now a POS chain and this is not as prevalent however the context of this vulnerability is still important to understand different attack flows for auditors. Transaction Order Dependence (TOD) is a vulnerability in smart contracts that arises when the execution outcome of a contract function depends on the order of transactions.
**2** | [Denial of Service (Unexpected Revert)](/days/day2.md) | This vulnerability arises when a function that's meant to execute a task returns an unexpected error (reverts), due to some exceptional condition or programming mistake; halting execution of the smart contract and returning the remaining gas.
**3** | [Denial of Service (Block Gas Limit)](/days/day3.md) | This vulnerability exists when an excessive amount of gas is used to execute a transaction causing it to fail due to reaching the maximum gas limit, effectively rendering the contract unusable and causing a denial of service for other users.
**4** | [Reentrancy - Simple](/days/day4.md) | This vulnerability is introduced when an external call is performed to another contract as it can lead to a change in control flow and changes to the data of the calling function that were not intended
**5** | [Reentrancy - Cross-Functional](https://medium.com/valixconsulting/solidity-smart-contract-security-by-example-04-cross-function-reentrancy-de9cbce0558e) | This form of reentrancy occurs when a function can be called recursively and another function is called in between the calls. 
**6** | [Reentrancy - Cross-Contract](https://medium.com/valixconsulting/solidity-smart-contract-security-by-example-05-cross-contract-reentrancy-30f29e2a01b9) | This form of reentrancy occurs when multiple contracts share the same state variable, and some contracts update that variable insecurely.
**7** | [Selfdestruct (Unexpected Ether)](https://twitter.com/theweb3hacker/status/1626821990144172033) | The selfdestruct function removes all bytecode from the contract address and sends all ether stored there to the address specified by the parameter called with the function. If the specified address is also a contract, no functions (including the fallback) get called.
**8** | [Improper Checks for EOA](/days/day8.md) | The EXTCODESIZE opcode is used in the Ethereum Virtual Machine (EVM) to determine the size of an account's code. For example, if the size of the caller's code is greater than 0, then the address according to EXTCODESIZE is assumed to be a contract. If not, then it is considered an EOA. However, relying on EXTCODESIZE to differentiate between EOAs and smart contracts can lead to potential vulnerabilities and unexpected behavior as this opcode can be subverted in certain sceenarios.
**9** | [Improper Access Control](/days/day9.md) | Access control vulnerabilities in Solidity occur when a smart contract does not properly restrict access to sensitive functions or data. This can lead to unauthorized actions being performed by malicious users or other contracts, compromising the contract's security and integrity.
**10** | [Unencrypted Private Data](/days/day10.md) | Unencrypted private data vulnerability in Solidity occurs when sensitive data is stored on the blockchain without encryption. Due to the transparent nature of the blockchain, all data stored within contracts, including private variables, can be accessed by anyone with access to the network.
**11** | [Controlled Delegate Call](/days/day11.md) | This vulnerability occurs when a contract uses the delegatecall opcode in an unsafe manner, allowing an attacker to control the target contract address or the function to be called.
**12** | [Signature Malleability](/days/day12.md) | This vulnerability allows an attacker to change the signature slightly without invalidating the signature itself. This often happens when a smart contract doesn't validate signatures properly, enabling attackers to modify them and potentially bypass security measures.
**13** | [Price Oracle Manipulation](/days/day13.md) | This vulnerability occurs when a smart contract relies on an external data source (an oracle) to provide information, such as prices for tokens, and an attacker manipulates that data source to provide false information, leading to unintended consequences in the smart contract execution.
