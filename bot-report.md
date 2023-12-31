# Winning bot race submission
  This is the top-ranked automated findings report, from henry bot. All findings in this report will be considered known issues for the purposes of your C4 audit.

  ## Summary 
| |Issue|Instances| Gas Savings
|-|:-|:-:|:-:|
| [[M&#x2011;01](#M-01)] | Centralization risk for privileged functions | 5| 0|
| |Issue|Instances| Gas Savings
|-|:-|:-:|:-:|
| [[L&#x2011;01](#L-01)] | Use `increaseAllowance()`/`decreaseAllowance()` instead of `approve()`/`safeApprove()` | 1| 0|
| [[L&#x2011;02](#L-02)] | Use of `tx.origin` is unsafe in almost every context | 2| 0|
| [[L&#x2011;03](#L-03)] | Variables shadowing other definitions | 4| 0|
| [[L&#x2011;04](#L-04)] | Missing zero address check in constructor | 3| 0|
| [[L&#x2011;05](#L-05)] | Solidity version 0.8.20 or above may not work on other chains due to PUSH0 | 2| 0|
| [[L&#x2011;06](#L-06)] | Using `>`/`>=` without specifying an upper bound in version pragma is unsafe | 2| 0|
| [[L&#x2011;07](#L-07)] | Tokens may be minted to the zero address | 1| 0|
| [[L&#x2011;08](#L-08)] | Consider implementing two-step procedure for updating protocol addresses | 2| 0|
| [[L&#x2011;09](#L-09)] | Vulnerable versions of packages are being used | 1| 0|
| [[L&#x2011;10](#L-10)] | Missing checks for `address(0)` when setting address state variables | 3| 0|
| [[L&#x2011;11](#L-11)] | Owner can renounce Ownership | 3| 0|
| [[L&#x2011;12](#L-12)] | Constructor / initialization function lacks parameter validation | 1| 0|
| [[L&#x2011;13](#L-13)] | Contracts are vulnerable to fee-on-transfer accounting-related issues | 13| 0|
| [[L&#x2011;14](#L-14)] | Functions calling contracts/addresses with transfer hooks should be protected by reentrancy guard | 13| 0|
| [[L&#x2011;15](#L-15)] | Critical functions should be controlled by time locks | 2| 0|
| [[L&#x2011;16](#L-16)] | The safeApprove() function is deprecated | 1| 0|
| [[L&#x2011;17](#L-17)] | Some tokens may revert when zero value transfers are made | 9| 0|
| [[L&#x2011;18](#L-18)] | Loss of precision in divisions | 1| 0|
| [[L&#x2011;19](#L-19)] | Code does not follow the best practice of check-effects-interaction | 10| 0|
| [[L&#x2011;20](#L-20)] | Some tokens may revert when large transfers are made | 13| 0|
| [[L&#x2011;21](#L-21)] | Contracts are vulnerable to rebasing accounting-related issues | 9| 0|
| |Issue|Instances| Gas Savings
|-|:-|:-:|:-:|
| [[G&#x2011;01](#G-01)] | Using `private` for constants saves gas | 3| 10218|
| [[G&#x2011;02](#G-02)] | Constructors can be marked as payable to save deployment gas | 4| 84|
| [[G&#x2011;03](#G-03)] | Using `++X`/`--X` instead of `X++`/`X--` can save gas | 1| 5|
| [[G&#x2011;04](#G-04)] | Use custom errors rather than `revert()`/`require()` strings to save gas | 12| 600|
| [[G&#x2011;05](#G-05)] | Do not cache state variables that are used only once | 4| 12|
| [[G&#x2011;06](#G-06)] | Inline `modifier`s that are only used once to save gas | 1| 0|
| [[G&#x2011;07](#G-07)] | Functions that revert when called by normal users can be marked `payable` | 6| 126|
| [[G&#x2011;08](#G-08)] | Use `x = x + y` instead of `x += y` for state variables | 1| 10|
| [[G&#x2011;09](#G-09)] | Operator `>=`/`<=` costs less gas than operator `>`/`<` | 6| 18|
| [[G&#x2011;10](#G-10)] | Unused non-constant state variables waste gas | 1| 0|
| [[G&#x2011;11](#G-11)] | Usage of `int`s/`uint`s smaller than 32 bytes incurs overhead | 1| 55|
| [[G&#x2011;12](#G-12)] | Divisions can be unchecked to save gas | 8| 160|
| [[G&#x2011;13](#G-13)] | Increments can be `unchecked` to save gas | 1| 60|
| [[G&#x2011;14](#G-14)] | Use assembly to validate `msg.sender` | 3| 36|
| [[G&#x2011;15](#G-15)] | Using assembly to check for zero can save gas | 5| 30|
| [[G&#x2011;16](#G-16)] | Avoid contract existence checks by using low level calls | 8| 800|
| [[G&#x2011;17](#G-17)] | Use `uint256(1)`/`uint256(2)` instead of `true`/`false` to save gas for changes | 4| 68400|
| [[G&#x2011;18](#G-18)] | Avoid zero transfer to save gas | 9| 900|
| [[G&#x2011;19](#G-19)] | Optimize names to save gas | 4| 88|
| [[G&#x2011;20](#G-20)] | Reduce gas usage by moving to Solidity 0.8.19 or later | 2| 0|
| [[G&#x2011;21](#G-21)] | Newer versions of solidity are more gas efficient | 4| 0|
| [[G&#x2011;22](#G-22)] | Avoid updating storage when the value hasn't changed | 5| 4000|
| [[G&#x2011;23](#G-23)] | State variables that are used multiple times in a function should be cached in stack variables | 4| 1164|
| [[G&#x2011;24](#G-24)] | Contracts can use fewer storage slots by truncating state variables | 1| 20000|
| [[G&#x2011;25](#G-25)] | Refactor duplicated `require()`/`revert()` checks to save gas | 1| 0|
| [[G&#x2011;26](#G-26)] | Use assembly to emit events | 9| 342|
| [[G&#x2011;27](#G-27)] | Use `calldata` instead of `memory` for immutable arguments | 2| 1200|
| [[G&#x2011;28](#G-28)] | Using `bool`s for storage incurs overhead | 4| 400|
| [[G&#x2011;29](#G-29)] | Multiple accesses of the same mapping/array key/index should be cached | 13| 924|
| [[G&#x2011;30](#G-30)] | Multiple mappings can be replaced with a single struct mapping | 4| 168|
| |Issue|Instances| Gas Savings
|-|:-|:-:|:-:|
| [[N&#x2011;01](#N-01)] | NatSpec documentation for contract is missing | 4| 0|
| [[N&#x2011;02](#N-02)] | Names of `private`/`internal` functions should be prefixed with an underscore | 1| 0|
| [[N&#x2011;03](#N-03)] | Order of functions does not follow the Solidity Style Guide | 13| 0|
| [[N&#x2011;04](#N-04)] | Use of `override` is unnecessary | 2| 0|
| [[N&#x2011;05](#N-05)] | Custom errors should be used rather than `revert()`/`require()` | 12| 0|
| [[N&#x2011;06](#N-06)] | Large numeric literals should use underscores for readability | 6| 0|
| [[N&#x2011;07](#N-07)] | Assembly blocks should have extensive comments | 1| 0|
| [[N&#x2011;08](#N-08)] | Simplify complex require statements | 1| 0|
| [[N&#x2011;09](#N-09)] | Consider moving `msg.sender` checks to `modifier`s | 2| 0|
| [[N&#x2011;10](#N-10)] | Consider adding a block/deny-list | 2| 0|
| [[N&#x2011;11](#N-11)] | Constants/Immutables redefined elsewhere | 2| 0|
| [[N&#x2011;12](#N-12)] | Convert simple `if`-statements to ternary expressions | 1| 0|
| [[N&#x2011;13](#N-13)] | Events should be emitted before external calls | 8| 0|
| [[N&#x2011;14](#N-14)] | Events are emitted without the sender information | 3| 0|
| [[N&#x2011;15](#N-15)] | Event is missing `indexed` fields | 3| 0|
| [[N&#x2011;16](#N-16)] | Imports could be organized more systematically | 4| 0|
| [[N&#x2011;17](#N-17)] | @openzeppelin/contracts should be upgraded to a newer version | 6| 0|
| [[N&#x2011;18](#N-18)] | Lines are too long | 11| 0|
| [[N&#x2011;19](#N-19)] | Magic numbers should be replaced with constants | 14| 0|
| [[N&#x2011;20](#N-20)] | Memory-safe annotation preferred over comment variant | 1| 0|
| [[N&#x2011;21](#N-21)] | Use `@inheritdoc` for overridden functions | 2| 0|
| [[N&#x2011;22](#N-22)] | Contracts should have NatSpec `@author` tags | 4| 0|
| [[N&#x2011;23](#N-23)] | Contracts should have `@notice` tags | 4| 0|
| [[N&#x2011;24](#N-24)] | Contracts should have NatSpec `@title` tags | 4| 0|
| [[N&#x2011;25](#N-25)] | Events missing NatSpec `@param` tag | 12| 0|
| [[N&#x2011;26](#N-26)] | Event declarations should have NatSpec descriptions | 12| 0|
| [[N&#x2011;27](#N-27)] | Functions missing NatSpec `@param` tag | 7| 0|
| [[N&#x2011;28](#N-28)] | NatSpec documentation for function is missing | 5| 0|
| [[N&#x2011;29](#N-29)] | Functions missing NatSpec `@return` tag | 9| 0|
| [[N&#x2011;30](#N-30)] | State variables should have NatSpec descriptions | 6| 0|
| [[N&#x2011;31](#N-31)] | Contract name does not follow the Solidity Style Guide | 2| 0|
| [[N&#x2011;32](#N-32)] | Functions should be named in mixedCase style | 3| 0|
| [[N&#x2011;33](#N-33)] | Variable names for `immutable`s should use UPPER_CASE_WITH_UNDERSCORES | 4| 0|
| [[N&#x2011;34](#N-34)] | Missing zero address check in functions with address parameters | 3| 0|
| [[N&#x2011;35](#N-35)] | Constants should be put on the left side of comparisons | 11| 0|
| [[N&#x2011;36](#N-36)] | Large multiples of ten should use scientific notation | 4| 0|
| [[N&#x2011;37](#N-37)] | Non-interface files should use fixed compiler versions | 2| 0|
| [[N&#x2011;38](#N-38)] | Unused contract variables | 1| 0|
| [[N&#x2011;39](#N-39)] | Unused import | 1| 0|
| [[N&#x2011;40](#N-40)] | Consider using `delete` rather than assigning zero to clear values | 2| 0|
| [[N&#x2011;41](#N-41)] | Use the latest Solidity version | 4| 0|
| [[N&#x2011;42](#N-42)] | Named mappings are recommended | 10| 0|
| [[N&#x2011;43](#N-43)] | Whitespace in Expressions | 1| 0|
| [[N&#x2011;44](#N-44)] | Modifier declarations should have NatSpec descriptions | 1| 0|
| [[N&#x2011;45](#N-45)] | Contract functions should use an `interface` | 18| 0|
| [[N&#x2011;46](#N-46)] | Addresses shouldn't be hard-coded | 3| 0|
| [[N&#x2011;47](#N-47)] | Multiple mappings with same keys can be combined into a single struct mapping for readability | 4| 0|
| [[N&#x2011;48](#N-48)] | Control structures do not follow the Solidity Style Guide | 1| 0|
| [[N&#x2011;49](#N-49)] | Do not cache immutable variables | 2| 0|
| [[N&#x2011;50](#N-50)] | Missing event for critical changes | 1| 0|
| [[N&#x2011;51](#N-51)] | Duplicated `require()`/`revert()` checks should be refactored | 1| 0|
| [[N&#x2011;52](#N-52)] | Consider adding emergency-stop functionality | 3| 0|
| [[N&#x2011;53](#N-53)] | Avoid the use of sensitive terms | 23| 0|
| [[N&#x2011;54](#N-54)] | Contracts should have NatSpec `@dev` tags | 4| 0|
| [[N&#x2011;55](#N-55)] | Missing NatSpec `@dev` from event declaration | 12| 0|
| [[N&#x2011;56](#N-56)] | Missing NatSpec `@notice` from event declaration | 12| 0|
| [[N&#x2011;57](#N-57)] | Missing NatSpec `@dev` from function declaration | 23| 0|
| [[N&#x2011;58](#N-58)] | Missing NatSpec `@notice` from function declaration | 5| 0|
| [[N&#x2011;59](#N-59)] | Missing NatSpec `@dev` from modifier declaration | 1| 0|
| [[N&#x2011;60](#N-60)] | Missing NatSpec `@notice` from modifier declaration | 1| 0|
| [[N&#x2011;61](#N-61)] | Contracts should have full test coverage | 1| 0|
| [[N&#x2011;62](#N-62)] | Large or complicated code bases should implement invariant tests | 1| 0|
| [[N&#x2011;63](#N-63)] | Top-level declarations should be separated by at least two lines | 12| 0|
| [[N&#x2011;64](#N-64)] | Consider adding formal verification proofs | 4| 1000|
| [[N&#x2011;65](#N-65)] | Error messages should be descriptive, not cryptic | 6| 18|
| |Issue|Instances| Gas Savings
|-|:-|:-:|:-:|
| [[D&#x2011;01](#D-01)] | Using `private` rather than `public` for constants, saves gas | 4| 0|
| [[D&#x2011;02](#D-02)] | Event names should use CamelCase | 12| 0|
| [[D&#x2011;03](#D-03)] | Avoid double casting | 1| 0|
| [[D&#x2011;04](#D-04)] | Event is missing `indexed` fields | 1| 0|
| [[D&#x2011;05](#D-05)] | `internal` functions only called once can be inlined to save gas | 1| 30|
| [[D&#x2011;06](#D-06)] | Variables should be named in mixedCase style | 1| 0|
| [[D&#x2011;07](#D-07)] | safeMint should be used in place of mint | 3| 0|
| [[D&#x2011;08](#D-08)] | `x += y` is more expensive than `x = x + y` for state variables | 12| 0|
| [[D&#x2011;09](#D-09)] | Revert on transfer to the zero address | 13| 0|
| [[D&#x2011;10](#D-10)] | `SafeTransferLib` does not ensure that the token contract exists | 14| 0|
| [[D&#x2011;11](#D-11)] | Solidity version 0.8.20 or above may not work on other chains due to PUSH0 | 2| 0|
| [[D&#x2011;12](#D-12)] | SPDX identifier should be the in the first line of a solidity file | 4| 0|
| [[D&#x2011;13](#D-13)] | Numbers downcast to `address`es may result in collisions | 8| 0|
| [[D&#x2011;14](#D-14)] | Unused named return | 1| 0|
| [[D&#x2011;15](#D-15)] | Unused named return variables without optimizer waste gas | 1| 9|
| [[D&#x2011;16](#D-16)] | Using bitmap to store bool states can save gas | 3| 0|
| [[D&#x2011;17](#D-17)] | Using `delete` statement can save gas | 2| 16|
| [[D&#x2011;18](#D-18)] | Use `!= 0` or `== 0` for unsigned integer comparison | 4| 0|
| [[D&#x2011;19](#D-19)] | Avoid contract existence checks by using low level calls | 6| 0|
| [[D&#x2011;20](#D-20)] | Use Ownable2Step instead of Ownable | 3| 0|
| [[D&#x2011;21](#D-21)] | Events that mark critical parameter changes should contain both the old and the new value | 1| 0|
| [[D&#x2011;22](#D-22)] | `safeTransfer` function does not check for contract existence | 4| 0|
| [[D&#x2011;23](#D-23)] | Assembly block creates dirty bits | 1| 0|
| [[D&#x2011;24](#D-24)] | `require()` or `revert()` statements that check input arguments should be at the top of the function | 4| 0|
| [[D&#x2011;25](#D-25)] | Division by zero not prevented | 1| 0|
| [[D&#x2011;26](#D-26)] | Inconsistent spacing in comments | 4| 0|
| [[D&#x2011;27](#D-27)] | Consider activating via-ir for deploying | 1| 0|
| [[D&#x2011;28](#D-28)] | Enable IR-based code generation | 1| 0|
| [[D&#x2011;29](#D-29)] | Large approvals may not work with some `ERC20` tokens | 1| 0|
| [[D&#x2011;30](#D-30)] | Contracts are vulnerable to rebasing accounting-related issues | 1| 0|
 Audit report generated by Bot-Henry. ### Medium Risk Issues


### [M&#x2011;01]<a name="M-01"></a> Centralization risk for privileged functions
Contracts with privileged functions need owner/admin to be trusted not to perform malicious updates or drain funds. This may also cause a single point failure.

*There are 5 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}104:     function changeBondingCurveAllowed(address _bondingCurve, bool _newState) external onlyOwner {

244:     function claimPlatformFee() external onlyOwner {

300:     function restrictShareCreation(bool _isRestricted) external onlyOwner {

309:     function changeShareCreatorWhitelist(address _address, bool _isWhitelisted) external onlyOwner {
```


*GitHub* : [104](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L104),[244](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L244),[300](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L300),[309](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L309)

```solidity
File: asD/src/asD.sol

}72:     function withdrawCarry(uint256 _amount) external onlyOwner {
```


*GitHub* : [72](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L72)### Low Risk Issues


### [L&#x2011;01]<a name="L-01"></a> Use `increaseAllowance()`/`decreaseAllowance()` instead of `approve()`/`safeApprove()`
Changing an allowance with `approve()` brings the risk that someone may use both the old and the new allowance by unfortunate transaction ordering. Refer to [ERC20 API: An Attack Vector on the Approve/TransferFrom Methods](https://docs.google.com/document/d/1YLPtQxZu1UAvO9cZ1O2RPXBbT0mooh4DYKjA_jp-RLM).
It is recommended to use the `increaseAllowance()`/`decreaseAllowance()` to avoid ths problem.

*There are 1 instance(s) of this issue:*

```solidity
File: asD/src/asD.sol

}51:         SafeERC20.safeApprove(note, cNote, _amount);
```


*GitHub* : [51](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L51)
### [L&#x2011;02]<a name="L-02"></a> Use of `tx.origin` is unsafe in almost every context
According to [Vitalik Buterin](https://ethereum.stackexchange.com/questions/196/how-do-i-make-my-dapp-serenity-proof), contracts should _not_ `assume that tx.origin will continue to be usable or meaningful`. An example of this is [EIP-3074](https://eips.ethereum.org/EIPS/eip-3074#allowing-txorigin-as-signer-1) which explicitly mentions the intention to change its semantics when it's used with new op codes. There have also been calls to [remove](https://github.com/ethereum/solidity/issues/683) `tx.origin`, and there are [security issues](solidity.readthedocs.io/en/v0.4.24/security-considerations.html#tx-origin) associated with using it for authorization. For these reasons, it's best to completely avoid the feature.

*There are 2 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}96:             turnstile.register(tx.origin);
```


*GitHub* : [96](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L96)

```solidity
File: asD/src/asDFactory.sol

}29:             turnstile.register(tx.origin);
```


*GitHub* : [29](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L29)
### [L&#x2011;03]<a name="L-03"></a> Variables shadowing other definitions
A variable declaration shadowing any other existing definition is error-prone. It can cause confusion for developers, potentially introduce bugs, and reduce the readability and maintainability.

*There are 4 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}/// @audit Shadows `state variable _uri`
91:     constructor(string memory _uri, address _paymentToken) ERC1155(_uri) Ownable() {
```


*GitHub* : [91](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L91)

```solidity
File: asD/src/asD.sol

}/// @audit Shadows `state variable _name`
29:         string memory _name,

/// @audit Shadows `state variable _symbol`
30:         string memory _symbol,

/// @audit Shadows `state variable _owner`
31:         address _owner,
```


*GitHub* : [29](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L29),[30](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L30),[31](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L31)
### [L&#x2011;04]<a name="L-04"></a> Missing zero address check in constructor
Constructors often take address parameters to initialize important components of a contract, such as owner or linked contracts. However, without a checking, there's a risk that an address parameter could be mistakenly set to the zero address (0x0). This could be due to an error or oversight during contract deployment. A zero address in a crucial role can cause serious issues, as it cannot perform actions like a normal address, and any funds sent to it will be irretrievable. It's therefore crucial to include a zero address check in constructors to prevent such potential problems. If a zero address is detected, the constructor should revert the transaction.

*There are 3 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}/// @audit `_paymentToken not checked`
91:     constructor(string memory _uri, address _paymentToken) ERC1155(_uri) Ownable() {
```


*GitHub* : [91](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L91)

```solidity
File: asD/src/asD.sol

}/// @audit `_owner not checked`
/// @audit `_cNote not checked`
/// @audit `_csrRecipient not checked`
28:     constructor(
29:         string memory _name,
30:         string memory _symbol,
31:         address _owner,
32:         address _cNote,
33:         address _csrRecipient
34:     ) ERC20(_name, _symbol) {
```


*GitHub* : [28-34](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L28-L34)

```solidity
File: asD/src/asDFactory.sol

}/// @audit `_cNote not checked`
24:     constructor(address _cNote) {
```


*GitHub* : [24](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L24)
### [L&#x2011;05]<a name="L-05"></a> Solidity version 0.8.20 or above may not work on other chains due to PUSH0
Solidity version 0.8.20 or above uses the new [Shanghai EVM](https://blog.soliditylang.org/2023/05/10/solidity-0.8.20-release-announcement/#important-note) which introduces the PUSH0 opcode. This op code may not yet be implemented on all evm-chains or Layer2s, so deployment on these chains will fail. Consider using an earlier solidity version.

*There are 2 instance(s) of this issue:*

```solidity
File: asD/src/asD.sol

}2: pragma solidity >=0.8.0;
```


*GitHub* : [2](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L2)

```solidity
File: asD/src/asDFactory.sol

}2: pragma solidity >=0.8.0;
```


*GitHub* : [2](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L2)
### [L&#x2011;06]<a name="L-06"></a> Using `>`/`>=` without specifying an upper bound in version pragma is unsafe
There **will** be breaking changes in future versions of solidity, and at that point your code will no longer be compatible. While you may have the specific version to use in a configuration file, others that include your source files may not.

*There are 2 instance(s) of this issue:*

```solidity
File: asD/src/asD.sol

}2: pragma solidity >=0.8.0;
```


*GitHub* : [2](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L2)

```solidity
File: asD/src/asDFactory.sol

}2: pragma solidity >=0.8.0;
```


*GitHub* : [2](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L2)
### [L&#x2011;07]<a name="L-07"></a> Tokens may be minted to the zero address
The target address is not checked in the mint function.

*There are 1 instance(s) of this issue:*

```solidity
File: asD/src/asD.sol

}47:     function mint(uint256 _amount) external {
48:         CErc20Interface cNoteToken = CErc20Interface(cNote);
49:         IERC20 note = IERC20(cNoteToken.underlying());
50:         SafeERC20.safeTransferFrom(note, msg.sender, address(this), _amount);
51:         SafeERC20.safeApprove(note, cNote, _amount);
52:         uint256 returnCode = cNoteToken.mint(_amount);
53:         // Mint returns 0 on success: https://docs.compound.finance/v2/ctokens/#mint
54:         require(returnCode == 0, "Error when minting");
55:         _mint(msg.sender, _amount);
56:     }
```


*GitHub* : [47-56](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L47-L56)
### [L&#x2011;08]<a name="L-08"></a> Consider implementing two-step procedure for updating protocol addresses
A copy-paste error or a typo may end up bricking protocol functionality, or sending tokens to an address with no known private key. Consider implementing a two-step procedure for updating protocol addresses, where the recipient is set as pending, and must 'accept' the assignment by making an affirmative call. A straight forward way of doing this would be to have the target contracts implement [EIP-165](https://eips.ethereum.org/EIPS/eip-165), and to have the 'set' functions ensure that the recipient is of the right interface type.

*There are 2 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}104:     function changeBondingCurveAllowed(address _bondingCurve, bool _newState) external onlyOwner {
105:         require(whitelistedBondingCurves[_bondingCurve] != _newState, "State already set");
106:         whitelistedBondingCurves[_bondingCurve] = _newState;
107:         emit BondingCurveStateChange(_bondingCurve, _newState);
108:     }

309:     function changeShareCreatorWhitelist(address _address, bool _isWhitelisted) external onlyOwner {
310:         require(whitelistedShareCreators[_address] != _isWhitelisted, "State already set");
311:         whitelistedShareCreators[_address] = _isWhitelisted;
312:     }
```


*GitHub* : [104-108](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L104-L108),[309-312](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L309-L312)
### [L&#x2011;09]<a name="L-09"></a> Vulnerable versions of packages are being used
This project is using specific package versions which are vulnerable to the specific CVEs listed below. Consider switching to more recent versions of these packages that don't have these vulnerabilities.
- [CVE-2023-40014](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2023-40014) - **MEDIUM** - (`openzeppelin-solidity >=4.0.0 <4.9.3`): OpenZeppelin Contracts is a library for secure smart contract development. Starting in version 4.0.0 and prior to version 4.9.3, contracts using `ERC2771Context` along with a custom trusted forwarder may see `_msgSender` return `address(0)` in calls that originate from the forwarder with calldata shorter than 20 bytes. This combination of circumstances does not appear to be common, in particular it is not the case for `MinimalForwarder` from OpenZeppelin Contracts, or any deployed forwarder the team is aware of, given that the signer address is appended to all calls that originate from these forwarders. The problem has been patched in v4.9.3.

- [CVE-2023-34459](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2023-34459) - **MEDIUM** - (`openzeppelin-solidity >=4.7.0 <4.9.2`): OpenZeppelin Contracts is a library for smart contract development. Starting in version 4.7.0 and prior to version 4.9.2, when the `verifyMultiProof`, `verifyMultiProofCalldata`, `procesprocessMultiProof`, or `processMultiProofCalldat` functions are in use, it is possible to construct merkle trees that allow forging a valid multiproof for an arbitrary set of leaves. A contract may be vulnerable if it uses multiproofs for verification and the merkle tree that is processed includes a node with value 0 at depth 1 (just under the root). This could happen inadvertedly for balanced trees with 3 leaves or less, if the leaves are not hashed. This could happen deliberately if a malicious tree builder includes such a node in the tree. A contract is not vulnerable if it uses single-leaf proving (`verify`, `verifyCalldata`, `processProof`, or `processProofCalldata`), or if it uses multiproofs with a known tree that has hashed leaves. Standard merkle trees produced or validated with the @openzeppelin/merkle-tree library are safe. The problem has been patched in version 4.9.2. Some workarounds are available. For those using multiproofs: When constructing merkle trees hash the leaves and do not insert empty nodes in your trees. Using the @openzeppelin/merkle-tree package eliminates this issue. Do not accept user-provided merkle roots without reconstructing at least the first level of the tree. Verify the merkle tree structure by reconstructing it from the leaves.

*There are 1 instance(s) of this issue:*

```solidity
/// @audit Global finding.
```


*GitHub* : [0](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1)
### [L&#x2011;10]<a name="L-10"></a> Missing checks for `address(0)` when setting address state variables
Consider adding a zero address check when setting address state variables.

*There are 3 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}92:         token = IERC20(_paymentToken);
```


*GitHub* : [92](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L92)

```solidity
File: asD/src/asD.sol

}36:         cNote = _cNote;
```


*GitHub* : [36](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L36)

```solidity
File: asD/src/asDFactory.sol

}25:         cNote = _cNote;
```


*GitHub* : [25](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L25)
### [L&#x2011;11]<a name="L-11"></a> Owner can renounce Ownership
Each of the following contracts implements or inherits the `renounceOwnership()` function. This can represent a certain risk if the ownership is renounced for any other reason than by design. Renouncing ownership will leave the contract without an owner, thereby removing any functionality that is only available to the owner.

*There are 3 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}10: contract Market is ERC1155, Ownable2Step {
11:     /*//////////////////////////////////////////////////////////////
12:                                  CONSTANTS
13:     //////////////////////////////////////////////////////////////*/
```


*GitHub* : [10-13](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L10-L13)

```solidity
File: asD/src/asD.sol

}11: contract asD is ERC20, Ownable2Step {
12:     /*//////////////////////////////////////////////////////////////
13:                                  STATE
14:     //////////////////////////////////////////////////////////////*/
```


*GitHub* : [11-14](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L11-L14)

```solidity
File: asD/src/asDFactory.sol

}8: contract asDFactory is Ownable2Step {
9:     /*//////////////////////////////////////////////////////////////
10:                                  STATE
11:     //////////////////////////////////////////////////////////////*/
```


*GitHub* : [8-11](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L8-L11)
### [L&#x2011;12]<a name="L-12"></a> Constructor / initialization function lacks parameter validation
Constructors and initialization functions play a critical role in contracts by setting important initial states when the contract is first deployed before the system starts. The parameters passed to the constructor and initialization functions directly affect the behavior of the contract / protocol. If incorrect parameters are provided, the system may fail to run, behave abnormally, be unstable, or lack security. Therefore, it's crucial to carefully check each parameter in the constructor and initialization functions. If an exception is found, the transaction should be rolled back.

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}/// @audit `_priceIncrease`
10:     constructor(uint256 _priceIncrease) {
```


*GitHub* : [10](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L10)
### [L&#x2011;13]<a name="L-13"></a> Contracts are vulnerable to fee-on-transfer accounting-related issues
Some tokens take a transfer fee (e.g. STA, PAXG), some do not currently charge a fee but may do so in the future (e.g. USDT, USDC).
The functions below transfer funds from the caller to the receiver via `transferFrom()`, but do not ensure that the actual number of tokens received is the same as the input amount to the transfer. If the token is a fee-on-transfer token, the balance after the transfer will be smaller than expected, leading to accounting issues. Even if there are checks later, related to a secondary transfer, an attacker may be able to use latent funds (e.g. mistakenly sent by another user) in order to get a free credit.
One way to solve this problem is to measure the balance before and after the transfer, and use the difference as the amount, rather than the stated amount.

*There are 13 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}153:         SafeERC20.safeTransferFrom(token, msg.sender, address(this), price + fee);

166:             SafeERC20.safeTransfer(token, msg.sender, rewardsSinceLastClaim);

187:         SafeERC20.safeTransfer(token, msg.sender, rewardsSinceLastClaim + price - fee);

206:         SafeERC20.safeTransferFrom(token, msg.sender, address(this), fee);

217:             SafeERC20.safeTransfer(token, msg.sender, rewardsSinceLastClaim);

229:         SafeERC20.safeTransferFrom(token, msg.sender, address(this), fee);

238:         SafeERC20.safeTransfer(token, msg.sender, rewardsSinceLastClaim);

247:         SafeERC20.safeTransfer(token, msg.sender, amount);

257:         SafeERC20.safeTransfer(token, msg.sender, amount);

267:             SafeERC20.safeTransfer(token, msg.sender, amount);
```


*GitHub* : [153](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L153),[166](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L166),[187](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L187),[206](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L206),[217](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L217),[229](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L229),[238](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L238),[247](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L247),[257](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L257),[267](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L267)

```solidity
File: asD/src/asD.sol

}50:         SafeERC20.safeTransferFrom(note, msg.sender, address(this), _amount);

66:         SafeERC20.safeTransfer(note, msg.sender, _amount);

88:         SafeERC20.safeTransfer(note, msg.sender, _amount);
```


*GitHub* : [50](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L50),[66](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L66),[88](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L88)
### [L&#x2011;14]<a name="L-14"></a> Functions calling contracts/addresses with transfer hooks should be protected by reentrancy guard
Even if the function follows the best practice of check-effects-interaction, not using a reentrancy guard when there may be transfer hooks opens the users of this protocol up to [read-only reentrancy vulnerability](https://chainsecurity.com/curve-lp-oracle-manipulation-post-mortem/) with no way to protect them except by block-listing the entire protocol.

*There are 13 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}153:         SafeERC20.safeTransferFrom(token, msg.sender, address(this), price + fee);

166:             SafeERC20.safeTransfer(token, msg.sender, rewardsSinceLastClaim);

187:         SafeERC20.safeTransfer(token, msg.sender, rewardsSinceLastClaim + price - fee);

206:         SafeERC20.safeTransferFrom(token, msg.sender, address(this), fee);

217:             SafeERC20.safeTransfer(token, msg.sender, rewardsSinceLastClaim);

229:         SafeERC20.safeTransferFrom(token, msg.sender, address(this), fee);

238:         SafeERC20.safeTransfer(token, msg.sender, rewardsSinceLastClaim);

247:         SafeERC20.safeTransfer(token, msg.sender, amount);

257:         SafeERC20.safeTransfer(token, msg.sender, amount);

267:             SafeERC20.safeTransfer(token, msg.sender, amount);
```


*GitHub* : [153](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L153),[166](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L166),[187](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L187),[206](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L206),[217](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L217),[229](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L229),[238](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L238),[247](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L247),[257](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L257),[267](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L267)

```solidity
File: asD/src/asD.sol

}50:         SafeERC20.safeTransferFrom(note, msg.sender, address(this), _amount);

66:         SafeERC20.safeTransfer(note, msg.sender, _amount);

88:         SafeERC20.safeTransfer(note, msg.sender, _amount);
```


*GitHub* : [50](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L50),[66](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L66),[88](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L88)
### [L&#x2011;15]<a name="L-15"></a> Critical functions should be controlled by time locks
It is a good practice to give time for users to react and adjust to critical changes. A timelock provides more guarantees and reduces the level of trust required, thus decreasing risk for users. It also indicates that the project is legitimate (less risk of a malicious owner making a sandwich attack on a user).

*There are 2 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}104:     function changeBondingCurveAllowed(address _bondingCurve, bool _newState) external onlyOwner {

309:     function changeShareCreatorWhitelist(address _address, bool _isWhitelisted) external onlyOwner {
```


*GitHub* : [104](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L104),[309](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L309)
### [L&#x2011;16]<a name="L-16"></a> The safeApprove() function is deprecated
The `safeApprove()` like function [is deprecated](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/bfff03c0d2a59bcd8e2ead1da9aed9edf0080d05/contracts/token/ERC20/utils/SafeERC20.sol#L38-L49).
It is encouraged to use `safeIncreaseAllowance()` and `safeDecreaseAllowance()` instead.

*There are 1 instance(s) of this issue:*

```solidity
File: asD/src/asD.sol

}51:         SafeERC20.safeApprove(note, cNote, _amount);
```


*GitHub* : [51](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L51)
### [L&#x2011;17]<a name="L-17"></a> Some tokens may revert when zero value transfers are made
Despite the fact that [EIP-20 states](https://github.com/ethereum/EIPs/blob/7500ac4fc1bbdfaf684e7ef851f798f6b667b2fe/EIPS/eip-20.md?plain=1#L116) that zero-value transfers must be accepted, some tokens, such as LEND, will revert if this is attempted, which may cause transactions that involve other tokens (such as batch operations) to fully revert. Consider skipping the transfer if the amount is zero, which will also save gas.

*There are 9 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}153:         SafeERC20.safeTransferFrom(token, msg.sender, address(this), price + fee);

187:         SafeERC20.safeTransfer(token, msg.sender, rewardsSinceLastClaim + price - fee);

206:         SafeERC20.safeTransferFrom(token, msg.sender, address(this), fee);

229:         SafeERC20.safeTransferFrom(token, msg.sender, address(this), fee);

238:         SafeERC20.safeTransfer(token, msg.sender, rewardsSinceLastClaim);

247:         SafeERC20.safeTransfer(token, msg.sender, amount);

257:         SafeERC20.safeTransfer(token, msg.sender, amount);
```


*GitHub* : [153](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L153),[187](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L187),[206](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L206),[229](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L229),[238](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L238),[247](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L247),[257](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L257)

```solidity
File: asD/src/asD.sol

}50:         SafeERC20.safeTransferFrom(note, msg.sender, address(this), _amount);

66:         SafeERC20.safeTransfer(note, msg.sender, _amount);
```


*GitHub* : [50](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L50),[66](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L66)
### [L&#x2011;18]<a name="L-18"></a> Loss of precision in divisions
Division by large numbers may result in the result being zero, due to solidity not supporting fractions. Consider requiring a minimum amount for the numerator to ensure that it is always larger than the denominator.

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}290:             shareData[_id].shareHolderRewardsPerTokenScaled += (shareHolderFee * 1e18) / _tokenCount;
```


*GitHub* : [290](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L290)
### [L&#x2011;19]<a name="L-19"></a> Code does not follow the best practice of check-effects-interaction
Code should follow the best-practice of [check-effects-interaction](https://blockchain-academy.hs-mittweida.de/courses/solidity-coding-beginners-to-intermediate/lessons/solidity-11-coding-patterns/topic/checks-effects-interactions/), where state variables are updated before any external calls are made. Doing so prevents a large class of reentrancy bugs.

*There are 10 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}/// @audit `safeTransferFrom()` is called on line 153
159:         rewardsLastClaimedValue[_id][msg.sender] = shareData[_id].shareHolderRewardsPerTokenScaled;

/// @audit `safeTransferFrom()` is called on line 153
161:         shareData[_id].tokenCount += _amount;

/// @audit `safeTransferFrom()` is called on line 153
162:         shareData[_id].tokensInCirculation += _amount;

/// @audit `safeTransferFrom()` is called on line 153
163:         tokensByAddress[_id][msg.sender] += _amount;

/// @audit `safeTransferFrom()` is called on line 206
210:         rewardsLastClaimedValue[_id][msg.sender] = shareData[_id].shareHolderRewardsPerTokenScaled;

/// @audit `safeTransferFrom()` is called on line 206
211:         tokensByAddress[_id][msg.sender] -= _amount;

/// @audit `safeTransferFrom()` is called on line 206
212:         shareData[_id].tokensInCirculation -= _amount;

/// @audit `safeTransferFrom()` is called on line 229
233:         rewardsLastClaimedValue[_id][msg.sender] = shareData[_id].shareHolderRewardsPerTokenScaled;

/// @audit `safeTransferFrom()` is called on line 229
234:         tokensByAddress[_id][msg.sender] += _amount;

/// @audit `safeTransferFrom()` is called on line 229
235:         shareData[_id].tokensInCirculation += _amount;
```


*GitHub* : [211](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L211),[235](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L235),[234](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L234),[233](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L233),[212](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L212),[210](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L210),[163](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L163),[162](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L162),[161](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L161),[159](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L159)
### [L&#x2011;20]<a name="L-20"></a> Some tokens may revert when large transfers are made
Tokens such as COMP or UNI will revert when an address' balance reaches [`type(uint96).max`](https://github.com/compound-finance/compound-protocol/blob/a3214f67b73310d547e00fc578e8355911c9d376/contracts/Governance/Comp.sol#L238). Ensure that the calls below can be broken up into smaller batches if necessary.

*There are 13 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}153:         SafeERC20.safeTransferFrom(token, msg.sender, address(this), price + fee);

166:             SafeERC20.safeTransfer(token, msg.sender, rewardsSinceLastClaim);

187:         SafeERC20.safeTransfer(token, msg.sender, rewardsSinceLastClaim + price - fee);

206:         SafeERC20.safeTransferFrom(token, msg.sender, address(this), fee);

217:             SafeERC20.safeTransfer(token, msg.sender, rewardsSinceLastClaim);

229:         SafeERC20.safeTransferFrom(token, msg.sender, address(this), fee);

238:         SafeERC20.safeTransfer(token, msg.sender, rewardsSinceLastClaim);

247:         SafeERC20.safeTransfer(token, msg.sender, amount);

257:         SafeERC20.safeTransfer(token, msg.sender, amount);

267:             SafeERC20.safeTransfer(token, msg.sender, amount);
```


*GitHub* : [166](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L166),[187](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L187),[206](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L206),[217](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L217),[229](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L229),[238](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L238),[247](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L247),[153](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L153),[257](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L257),[267](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L267)

```solidity
File: asD/src/asD.sol

}50:         SafeERC20.safeTransferFrom(note, msg.sender, address(this), _amount);

66:         SafeERC20.safeTransfer(note, msg.sender, _amount);

88:         SafeERC20.safeTransfer(note, msg.sender, _amount);
```


*GitHub* : [50](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L50),[66](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L66),[88](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L88)
### [L&#x2011;21]<a name="L-21"></a> Contracts are vulnerable to rebasing accounting-related issues
Rebasing tokens are tokens that have each holder's `balanceof()` increase over time. Aave aTokens are an example of such tokens. If rebasing tokens are used, rewards accrue to the contract holding the tokens, and cannot be withdrawn by the original depositor. To address the issue, track 'shares' deposited on a pro-rata basis, and let shares be redeemed for their proportion of the current balance at the time of the withdrawal.

*There are 9 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}150:     function buy(uint256 _id, uint256 _amount) external {

174:     function sell(uint256 _id, uint256 _amount) external {

203:     function mintNFT(uint256 _id, uint256 _amount) external {

226:     function burnNFT(uint256 _id, uint256 _amount) external {

244:     function claimPlatformFee() external onlyOwner {

253:     function claimCreatorFee(uint256 _id) external {

263:     function claimHolderFee(uint256 _id) external {
```


*GitHub* : [150](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L150),[174](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L174),[203](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L203),[226](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L226),[244](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L244),[253](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L253),[263](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L263)

```solidity
File: asD/src/asD.sol

}47:     function mint(uint256 _amount) external {

60:     function burn(uint256 _amount) external {
```


*GitHub* : [47](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L47),[60](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L60)### Gas Risk Issues


### [G&#x2011;01]<a name="G-01"></a> Using `private` for constants saves gas
If needed, the values can be read from the verified contract source code, or if there are multiple values there can be a single getter function that [returns a tuple](https://github.com/code-423n4/2022-08-frax/blob/90f55a9ce4e25bceed3a74290b854341d8de6afa/src/contracts/FraxlendPair.sol#L156-L178) of the values of all currently-public constants. Saves **3406-3606 gas** in deployment gas due to the compiler not having to create non-payable getter functions for deployment calldata, not having to store the bytes of the value outside of where it's used, and not adding another entry to the method ID table

*There are 3 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}14:     uint256 public constant NFT_FEE_BPS = 1_000; // 10%

15:     uint256 public constant HOLDER_CUT_BPS = 3_300; // 33%

16:     uint256 public constant CREATOR_CUT_BPS = 3_300; // 33%
```


*GitHub* : [16](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L16),[15](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L15),[14](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L14)
### [G&#x2011;02]<a name="G-02"></a> Constructors can be marked as payable to save deployment gas
Payable functions cost less gas to execute, because the compiler does not have to add extra checks to ensure that no payment is provided. A constructor can be safely marked as payable, because only the deployer would be able to pass funds, and the project itself would not pass any funds.

*There are 4 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}91:     constructor(string memory _uri, address _paymentToken) ERC1155(_uri) Ownable() {
```


*GitHub* : [91](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L91)

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}10:     constructor(uint256 _priceIncrease) {
```


*GitHub* : [10](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L10)

```solidity
File: asD/src/asD.sol

}28:     constructor(
29:         string memory _name,
30:         string memory _symbol,
31:         address _owner,
32:         address _cNote,
33:         address _csrRecipient
34:     ) ERC20(_name, _symbol) {
```


*GitHub* : [28-34](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L28-L34)

```solidity
File: asD/src/asDFactory.sol

}24:     constructor(address _cNote) {
```


*GitHub* : [24](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L24)
### [G&#x2011;03]<a name="G-03"></a> Using `++X`/`--X` instead of `X++`/`X--` can save gas
It can save 5 gas for each execution / per iteration.

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}20:         for (uint256 i = shareCount; i < shareCount + amount; i++) {
```


*GitHub* : [20](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L20)
### [G&#x2011;04]<a name="G-04"></a> Use custom errors rather than `revert()`/`require()` strings to save gas
Custom errors are available from solidity version 0.8.4. Custom errors save [**~50 gas**](https://gist.github.com/IllIllI000/ad1bd0d29a0101b25e57c293b4b0c746) each time they're hit by [avoiding having to allocate and store the revert string](https://blog.soliditylang.org/2021/04/21/custom-errors/#errors-in-depth). Not defining the strings also save deployment gas.

*There are 12 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}81:         require(
82:             !shareCreationRestricted || whitelistedShareCreators[msg.sender] || msg.sender == owner(),
83:             "Not allowed"
84:         );

105:         require(whitelistedBondingCurves[_bondingCurve] != _newState, "State already set");

119:         require(whitelistedBondingCurves[_bondingCurve], "Bonding curve not whitelisted");

120:         require(shareIDs[_shareName] == 0, "Share already exists");

151:         require(shareData[_id].creator != msg.sender, "Creator cannot buy");

254:         require(shareData[_id].creator == msg.sender, "Not creator");

301:         require(shareCreationRestricted != _isRestricted, "State already set");

310:         require(whitelistedShareCreators[_address] != _isWhitelisted, "State already set");
```


*GitHub* : [310](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L310),[105](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L105),[119](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L119),[301](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L301),[151](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L151),[254](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L254),[81-84](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L81-L84),[120](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L120)

```solidity
File: asD/src/asD.sol

}54:         require(returnCode == 0, "Error when minting");

64:         require(returnCode == 0, "Error when redeeming"); // 0 on success: https://docs.compound.finance/v2/ctokens/#redeem-underlying

81:             require(_amount <= maximumWithdrawable, "Too many tokens requested");

86:         require(returnCode == 0, "Error when redeeming"); // 0 on success: https://docs.compound.finance/v2/ctokens/#redeem
```


*GitHub* : [86](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L86),[81](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L81),[64](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L64),[54](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L54)
### [G&#x2011;05]<a name="G-05"></a> Do not cache state variables that are used only once
It's cheaper to access the state variable directly if it is accessed only once. This can save the 3 gas cost of the extra stack allocation.

*There are 4 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}134:         address bondingCurve = shareData[_id].bondingCurve;

143:         address bondingCurve = shareData[_id].bondingCurve;

195:         address bondingCurve = shareData[_id].bondingCurve;

273:         uint256 lastClaimedValue = rewardsLastClaimedValue[_id][msg.sender];
```


*GitHub* : [143](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L143),[195](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L195),[134](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L134),[273](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L273)
### [G&#x2011;06]<a name="G-06"></a> Inline `modifier`s that are only used once to save gas
Inline `modifier`s that are only used once can save gas.

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}80:     modifier onlyShareCreator() {
```


*GitHub* : [80](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L80)
### [G&#x2011;07]<a name="G-07"></a> Functions that revert when called by normal users can be marked `payable`
If a function modifier such as `onlyOwner` is used, the function will revert if a normal user tries to pay the function. Marking the function as `payable` will lower the gas cost for legitimate callers because the compiler will not include checks for whether a payment was provided.
The extra opcodes avoided are: 
`CALLVALUE(2), DUP1(3), ISZERO(3), PUSH2(3), JUMPI(10), PUSH1(3), DUP1(3), REVERT(0), JUMPDEST(1), POP(2)` 
which cost an average of about 21 gas per call to the function, in addition to the extra deployment cost.

*There are 6 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}104:     function changeBondingCurveAllowed(address _bondingCurve, bool _newState) external onlyOwner {

114:     function createNewShare(
115:         string memory _shareName,
116:         address _bondingCurve,
117:         string memory _metadataURI
118:     ) external onlyShareCreator returns (uint256 id) {

244:     function claimPlatformFee() external onlyOwner {

300:     function restrictShareCreation(bool _isRestricted) external onlyOwner {

309:     function changeShareCreatorWhitelist(address _address, bool _isWhitelisted) external onlyOwner {
```


*GitHub* : [300](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L300),[104](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L104),[114-118](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L114-L118),[244](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L244),[309](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L309)

```solidity
File: asD/src/asD.sol

}72:     function withdrawCarry(uint256 _amount) external onlyOwner {
```


*GitHub* : [72](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L72)
### [G&#x2011;08]<a name="G-08"></a> Use `x = x + y` instead of `x += y` for state variables
Using the `x = x + y` instead of `x += y` for state simple state variables can save **10 gas**. The same applies to `-=`, `*=`, etc.

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}295:         platformPool += platformFee;
```


*GitHub* : [295](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L295)
### [G&#x2011;09]<a name="G-09"></a> Operator `>=`/`<=` costs less gas than operator `>`/`<`
The compiler uses opcodes `GT` and `ISZERO` for code that uses `>`, but only requires `LT` for `>=`. A similar behavior applies for `>`, which uses opcodes `LT` and `ISZERO`, but only requires `GT` for `<=`. It can [save **3 gas**](https://gist.github.com/IllIllI000/3dc79d25acccfa16dee4e83ffdc6ffde) for each.
It should be converted to the `<=`/`>=` equivalent when comparing against integer literals.

*There are 6 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}165:         if (rewardsSinceLastClaim > 0) {

216:         if (rewardsSinceLastClaim > 0) {

266:         if (amount > 0) {

289:         if (_tokenCount > 0) {
```


*GitHub* : [289](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L289),[266](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L266),[165](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L165),[216](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L216)

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}20:         for (uint256 i = shareCount; i < shareCount + amount; i++) {

29:         if (shareCount > 1) {
```


*GitHub* : [29](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L29),[20](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L20)
### [G&#x2011;10]<a name="G-10"></a> Unused non-constant state variables waste gas
If the variable is assigned a non-zero value, saves Gsset (**20000 gas**). If it's assigned a zero value, saves Gsreset (**2900 gas**). If the variable remains unassigned, there is no gas savings unless the variable is `public`, in which case the compiler-generated non-payable getter deployment cost is saved. If the state variable is overriding an interface's public function, mark the variable as `constant` or `immutable` so that it does not use a storage slot.

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}46:     mapping(uint256 => address) public shareBondingCurves;
```


*GitHub* : [46](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L46)
### [G&#x2011;11]<a name="G-11"></a> Usage of `int`s/`uint`s smaller than 32 bytes incurs overhead
Using `ints`/`uints` smaller than 32 bytes may cost more gas. This is because the EVM operates on 32 bytes at a time, so if an element is smaller than 32 bytes, the EVM must perform more operations to reduce the size of the element from 32 bytes to the desired size.

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}/// @audit uint256
27:     uint256 public shareCount;
```


*GitHub* : [27](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L27)
### [G&#x2011;12]<a name="G-12"></a> Divisions can be unchecked to save gas
The expression `type(int).min/(-1)` is the only case where division causes an overflow. Therefore, uncheck can be used to [save gas](https://gist.github.com/DadeKuma/3bc597338ae774b8b3bd43280d55271f) in scenarios where it is certain that such an overflow will not occur.

*There are 8 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}197:         fee = (priceForOne * _amount * NFT_FEE_BPS) / 10_000;

275:             ((shareData[_id].shareHolderRewardsPerTokenScaled - lastClaimedValue) * tokensByAddress[_id][msg.sender]) /
276:             1e18;

285:         uint256 shareHolderFee = (_fee * HOLDER_CUT_BPS) / 10_000;

286:         uint256 shareCreatorFee = (_fee * CREATOR_CUT_BPS) / 10_000;

290:             shareData[_id].shareHolderRewardsPerTokenScaled += (shareHolderFee * 1e18) / _tokenCount;
```


*GitHub* : [197](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L197),[285](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L285),[290](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L290),[286](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L286),[275-276](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L275-L276)

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}23:             fee += (getFee(i) * tokenPrice) / 1e18;

35:         return 1e17 / divisor;
```


*GitHub* : [23](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L23),[35](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L35)

```solidity
File: asD/src/asD.sol

}75:         uint256 maximumWithdrawable = (CTokenInterface(cNote).balanceOf(address(this)) * exchangeRate) /
76:             1e28 -
```


*GitHub* : [75-76](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L75-L76)
### [G&#x2011;13]<a name="G-13"></a> Increments can be `unchecked` to save gas
Using `unchecked` increments can save gas by bypassing the built-in overflow checks. This can save [30-40 gas](https://gist.github.com/hrkrshnn/ee8fabd532058307229d65dcd5836ddc#the-increment-in-for-loop-post-condition-can-be-made-unchecked) **per iteration**. So it is recommended to use `unchecked` increments when overflow is not possible.

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}20:         for (uint256 i = shareCount; i < shareCount + amount; i++) {
```


*GitHub* : [20](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L20)
### [G&#x2011;14]<a name="G-14"></a> Use assembly to validate `msg.sender`
We can use assembly to efficiently validate msg.sender with the least amount of opcodes necessary. For more details check the following report [Here](https://code4rena.com/reports/2023-05-juicebox#g-06-use-assembly-to-validate-msgsender)

*There are 3 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}82:             !shareCreationRestricted || whitelistedShareCreators[msg.sender] || msg.sender == owner(),

151:         require(shareData[_id].creator != msg.sender, "Creator cannot buy");

254:         require(shareData[_id].creator == msg.sender, "Not creator");
```


*GitHub* : [254](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L254),[82](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L82),[151](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L151)
### [G&#x2011;15]<a name="G-15"></a> Using assembly to check for zero can save gas
Using assembly to check for zero can save gas by allowing more direct access to the evm and reducing some of the overhead associated with high-level operations in solidity.

*There are 5 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}120:         require(shareIDs[_shareName] == 0, "Share already exists");
```


*GitHub* : [120](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L120)

```solidity
File: asD/src/asD.sol

}54:         require(returnCode == 0, "Error when minting");

64:         require(returnCode == 0, "Error when redeeming"); // 0 on success: https://docs.compound.finance/v2/ctokens/#redeem-underlying

78:         if (_amount == 0) {

86:         require(returnCode == 0, "Error when redeeming"); // 0 on success: https://docs.compound.finance/v2/ctokens/#redeem
```


*GitHub* : [54](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L54),[64](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L64),[78](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L78),[86](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L86)
### [G&#x2011;16]<a name="G-16"></a> Avoid contract existence checks by using low level calls
Prior to 0.8.10 the compiler inserted extra code, including EXTCODESIZE (100 gas), to check for contract existence for external function calls. In more recent solidity versions, the compiler will not insert these checks if the external call has a return value. Similar behavior can be achieved in earlier versions by using low-level calls, since low level calls never check for contract existence.

*There are 8 instance(s) of this issue:*

```solidity
File: asD/src/asD.sol

}49:         IERC20 note = IERC20(cNoteToken.underlying());

52:         uint256 returnCode = cNoteToken.mint(_amount);

62:         IERC20 note = IERC20(cNoteToken.underlying());

63:         uint256 returnCode = cNoteToken.redeemUnderlying(_amount); // Request _amount of NOTE (the underlying of cNOTE)

73:         uint256 exchangeRate = CTokenInterface(cNote).exchangeRateCurrent(); // Scaled by 1 * 10^(18 - 8 + Underlying Token Decimals), i.e. 10^(28) in our case

75:         uint256 maximumWithdrawable = (CTokenInterface(cNote).balanceOf(address(this)) * exchangeRate) /

85:         uint256 returnCode = CErc20Interface(cNote).redeemUnderlying(_amount);

87:         IERC20 note = IERC20(CErc20Interface(cNote).underlying());
```


*GitHub* : [87](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L87),[49](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L49),[52](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L52),[62](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L62),[63](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L63),[73](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L73),[75](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L75),[85](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L85)
### [G&#x2011;17]<a name="G-17"></a> Use `uint256(1)`/`uint256(2)` instead of `true`/`false` to save gas for changes
Use uint256(1) and uint256(2) for true/false to avoid a Gwarmaccess (100 gas), and to avoid Gsset (20000 gas) when changing from ‘false’ to ‘true’, after having been ‘true’ in the past. Refer to the [source](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/5ae630684a0f57de400ef69499addab4c32ac8fb/contracts/security/ReentrancyGuard.sol#L23-L27).

*There are 4 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}49:     mapping(address => bool) public whitelistedBondingCurves;

61:     bool public shareCreationRestricted = true;

64:     mapping(address => bool) public whitelistedShareCreators;
```


*GitHub* : [64](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L64),[49](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L49),[61](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L61)

```solidity
File: asD/src/asDFactory.sol

}15:     mapping(address => bool) public isAsD;
```


*GitHub* : [15](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L15)
### [G&#x2011;18]<a name="G-18"></a> Avoid zero transfer to save gas
In Solidity, unnecessary operations can waste gas. For example, a transfer function without a zero amount check uses gas even if called with a zero amount, since the contract state remains unchanged. Implementing a zero amount check avoids these unnecessary function calls, saving gas and improving efficiency.

*There are 9 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}153:         SafeERC20.safeTransferFrom(token, msg.sender, address(this), price + fee);

187:         SafeERC20.safeTransfer(token, msg.sender, rewardsSinceLastClaim + price - fee);

206:         SafeERC20.safeTransferFrom(token, msg.sender, address(this), fee);

229:         SafeERC20.safeTransferFrom(token, msg.sender, address(this), fee);

238:         SafeERC20.safeTransfer(token, msg.sender, rewardsSinceLastClaim);

247:         SafeERC20.safeTransfer(token, msg.sender, amount);

257:         SafeERC20.safeTransfer(token, msg.sender, amount);
```


*GitHub* : [247](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L247),[153](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L153),[187](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L187),[206](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L206),[229](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L229),[238](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L238),[257](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L257)

```solidity
File: asD/src/asD.sol

}50:         SafeERC20.safeTransferFrom(note, msg.sender, address(this), _amount);

66:         SafeERC20.safeTransfer(note, msg.sender, _amount);
```


*GitHub* : [66](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L66),[50](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L50)
### [G&#x2011;19]<a name="G-19"></a> Optimize names to save gas
`public`/`external` function names and `public` member variable names can be optimized to save gas. Below are the interfaces/abstract contracts that can be optimized so that the most frequently-called functions use the least amount of gas possible during method lookup. Method IDs that have two leading zero bytes can save 128 gas each during deployment, and renaming functions to have lower method IDs will save 22 gas per call, [per sorted position shifted](https://medium.com/joyso/solidity-how-does-function-name-affect-gas-consumption-in-smart-contract-47d270d8ac92).

*There are 4 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}/// @audit changeBondingCurveAllowed(), createNewShare(), getBuyPrice(), getSellPrice(), buy(), sell(), getNFTMintingPrice(), mintNFT(), burnNFT(), claimPlatformFee(), claimCreatorFee(), claimHolderFee(), restrictShareCreation(), changeShareCreatorWhitelist(), NFT_FEE_BPS, HOLDER_CUT_BPS, CREATOR_CUT_BPS, token, shareCount, shareIDs, shareData, shareBondingCurves, whitelistedBondingCurves, tokensByAddress, rewardsLastClaimedValue, platformPool, shareCreationRestricted, whitelistedShareCreators
10: contract Market is ERC1155, Ownable2Step {
```


*GitHub* : [10](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L10)

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}/// @audit getPriceAndFee(), getFee(), priceIncrease
6: contract LinearBondingCurve is IBondingCurve {
```


*GitHub* : [6](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L6)

```solidity
File: asD/src/asD.sol

}/// @audit mint(), burn(), withdrawCarry(), cNote
11: contract asD is ERC20, Ownable2Step {
```


*GitHub* : [11](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L11)

```solidity
File: asD/src/asDFactory.sol

}/// @audit create(), cNote, isAsD
8: contract asDFactory is Ownable2Step {
```


*GitHub* : [8](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L8)
### [G&#x2011;20]<a name="G-20"></a> Reduce gas usage by moving to Solidity 0.8.19 or later
Solidity version 0.8.19 introduced a number of gas optimizations, refer to the [Solidity 0.8.19 Release Announcement](https://soliditylang.org/blog/2023/02/22/solidity-0.8.19-release-announcement) for details.

*There are 2 instance(s) of this issue:*

```solidity
File: asD/src/asD.sol

}2: pragma solidity >=0.8.0;
```


*GitHub* : [2](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L2)

```solidity
File: asD/src/asDFactory.sol

}2: pragma solidity >=0.8.0;
```


*GitHub* : [2](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L2)
### [G&#x2011;21]<a name="G-21"></a> Newer versions of solidity are more gas efficient
The solidity language continues to pursue more efficient gas optimization schemes. Adopting a [newer version of solidity](https://github.com/ethereum/solc-js/tags) can be more gas efficient.

*There are 4 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}2: pragma solidity 0.8.19;
```


*GitHub* : [2](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L2)

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}2: pragma solidity 0.8.19;
```


*GitHub* : [2](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L2)

```solidity
File: asD/src/asD.sol

}2: pragma solidity >=0.8.0;
```


*GitHub* : [2](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L2)

```solidity
File: asD/src/asDFactory.sol

}2: pragma solidity >=0.8.0;
```


*GitHub* : [2](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L2)
### [G&#x2011;22]<a name="G-22"></a> Avoid updating storage when the value hasn't changed
Manipulating storage in solidity is gas-intensive. It can be optimized by avoiding unnecessary storage updates when the new value equals the existing value.
If the old value is equal to the new value, not re-storing the value will avoid a Gsreset (**2900 gas**), potentially at the expense of a Gcoldsload (**2100 gas**) or a Gwarmaccess (**100 gas**).

*There are 5 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}159:         rewardsLastClaimedValue[_id][msg.sender] = shareData[_id].shareHolderRewardsPerTokenScaled;

180:         rewardsLastClaimedValue[_id][msg.sender] = shareData[_id].shareHolderRewardsPerTokenScaled;

210:         rewardsLastClaimedValue[_id][msg.sender] = shareData[_id].shareHolderRewardsPerTokenScaled;

233:         rewardsLastClaimedValue[_id][msg.sender] = shareData[_id].shareHolderRewardsPerTokenScaled;

265:         rewardsLastClaimedValue[_id][msg.sender] = shareData[_id].shareHolderRewardsPerTokenScaled;
```


*GitHub* : [159](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L159),[265](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L265),[233](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L233),[210](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L210),[180](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L180)
### [G&#x2011;23]<a name="G-23"></a> State variables that are used multiple times in a function should be cached in stack variables
When performing multiple operations on a state variable in a function, it is recommended to cache it first. Either multiple reads or multiple writes to a state variable can save gas by caching it on the stack.
Caching of a state variable replaces each Gwarmaccess (100 gas) with a much cheaper stack read. Other less obvious fixes/optimizations include having local memory caches of state variable structs, or having local caches of state variable contracts/addresses.
*Saves 100 gas per instance*.

*There are 4 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}/// @audit shareData[_id].tokensInCirculation: 2 reads 1 writes
150:     function buy(uint256 _id, uint256 _amount) external {

/// @audit shareData[_id].tokensInCirculation: 2 reads 1 writes
174:     function sell(uint256 _id, uint256 _amount) external {

/// @audit shareData[_id].tokensInCirculation: 2 reads 1 writes
203:     function mintNFT(uint256 _id, uint256 _amount) external {

/// @audit shareData[_id].tokensInCirculation: 2 reads 1 writes
226:     function burnNFT(uint256 _id, uint256 _amount) external {
```


*GitHub* : [226](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L226),[203](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L203),[174](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L174),[150](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L150)
### [G&#x2011;24]<a name="G-24"></a> Contracts can use fewer storage slots by truncating state variables
Some state variables can be safely modified so that the contract uses fewer storage slots. Each saved slot can avoid an extra Gsset (**20000 gas**) for the first setting of the struct. Subsequent reads as well as writes have smaller gas savings.

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}/// @audit Truncate `shareCount` to `uint64`
/// @audit Fewer storage usage (10 slots -> 9 slots):
///        32 B: mapping(string => uint256) shareIDs
///        32 B: mapping(uint256 => ShareData) shareData
///        32 B: mapping(uint256 => address) shareBondingCurves
///        32 B: mapping(address => bool) whitelistedBondingCurves
///        32 B: mapping(uint256 => mapping(address => uint256)) tokensByAddress
///        32 B: mapping(uint256 => mapping(address => uint256)) rewardsLastClaimedValue
///        32 B: uint256 platformPool
///        32 B: mapping(address => bool) whitelistedShareCreators
///        4 B: uint64 shareCount
///        1 B: bool shareCreationRestricted
10: contract Market is ERC1155, Ownable2Step {
```


*GitHub* : [10](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L10)
### [G&#x2011;25]<a name="G-25"></a> Refactor duplicated `require()`/`revert()` checks to save gas
Duplicate `require()`/`revert()` checks can be refactored into a modifier or function, saving deployment costs.

*There are 1 instance(s) of this issue:*

```solidity
File: asD/src/asD.sol

}/// @audit Duplicated on line 86
64:         require(returnCode == 0, "Error when redeeming"); // 0 on success: https://docs.compound.finance/v2/ctokens/#redeem-underlying
```


*GitHub* : [64](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L64)
### [G&#x2011;26]<a name="G-26"></a> Use assembly to emit events
To efficiently emit events, it's possible to utilize assembly by making use of scratch space and the free memory pointer. This approach has the advantage of potentially avoiding the costs associated with memory expansion.

However, it's important to note that in order to safely optimize this process, it is preferable to cache and restore the free memory pointer.

A good example of such practice can be seen in [Solady's](https://github.com/Vectorized/solady/blob/main/src/tokens/ERC1155.sol#L167) codebase.

*There are 9 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}107:         emit BondingCurveStateChange(_bondingCurve, _newState);

126:         emit ShareCreated(id, _shareName, _bondingCurve, msg.sender);

220:         emit NFTsCreated(_id, msg.sender, _amount, fee);

240:         emit NFTsBurned(_id, msg.sender, _amount, fee);

248:         emit PlatformFeeClaimed(msg.sender, amount);

258:         emit CreatorFeeClaimed(msg.sender, _id, amount);

269:         emit HolderFeeClaimed(msg.sender, _id, amount);

303:         emit ShareCreationRestricted(_isRestricted);
```


*GitHub* : [258](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L258),[269](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L269),[303](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L303),[126](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L126),[220](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L220),[240](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L240),[248](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L248),[107](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L107)

```solidity
File: asD/src/asD.sol

}89:         emit CarryWithdrawal(_amount);
```


*GitHub* : [89](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L89)
### [G&#x2011;27]<a name="G-27"></a> Use `calldata` instead of `memory` for immutable arguments
Mark data types as `calldata` instead of `memory` where possible. This makes it so that the data is not automatically loaded into memory. If the data passed into the function does not need to be changed (like updating values in an array), it can be passed in as `calldata`. The one exception to this is if the argument must later be passed into another function that takes an argument that specifies `memory` storage.

*There are 2 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}/// @audit _shareName
/// @audit _metadataURI
114:     function createNewShare(
115:         string memory _shareName,
116:         address _bondingCurve,
117:         string memory _metadataURI
118:     ) external onlyShareCreator returns (uint256 id) {
```


*GitHub* : [114-118](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L114-L118)

```solidity
File: asD/src/asDFactory.sol

}/// @audit _name
/// @audit _symbol
33:     function create(string memory _name, string memory _symbol) external returns (address) {
```


*GitHub* : [33](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L33)
### [G&#x2011;28]<a name="G-28"></a> Using `bool`s for storage incurs overhead
[Booleans are more expensive than uint256](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/58f635312aa21f947cae5f8578638a85aa2519f5/contracts/security/ReentrancyGuard.sol#L23-L27) or any type that takes up a full word because each write operation emits an extra SLOAD to first read the slot's contents, replace the bits taken up by the boolean, and then write back. This is the compiler's defense against contract upgrades and pointer aliasing, and it cannot be disabled.
Use `uint256(0)` and `uint256(1)` for true/false to avoid a Gwarmaccess (**[100 gas](https://gist.github.com/IllIllI000/1b70014db712f8572a72378321250058)**) for the extra SLOAD.

*There are 4 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}49:     mapping(address => bool) public whitelistedBondingCurves;

61:     bool public shareCreationRestricted = true;

64:     mapping(address => bool) public whitelistedShareCreators;
```


*GitHub* : [64](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L64),[49](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L49),[61](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L61)

```solidity
File: asD/src/asDFactory.sol

}15:     mapping(address => bool) public isAsD;
```


*GitHub* : [15](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L15)
### [G&#x2011;29]<a name="G-29"></a> Multiple accesses of the same mapping/array key/index should be cached
The instances below point to the second+ access of a value inside a mapping/array, within a function. Caching a mapping's value in a local `storage` or `calldata` variable when the value is accessed [multiple times](https://gist.github.com/IllIllI000/ec23a57daa30a8f8ca8b9681c8ccefb0), saves **~42 gas per access** due to not having to recalculate the key's keccak256 hash (Gkeccak256 - **30 gas**) and that calculation's associated stack operations. Caching an array's struct avoids recalculating the array offsets into memory/calldata

*There are 13 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}/// @audit `whitelistedBondingCurves[_bondingCurve]` is also accessed on line 105
106:         whitelistedBondingCurves[_bondingCurve] = _newState;

/// @audit `shareIDs[_shareName]` is also accessed on line 120
122:         shareIDs[_shareName] = id;

/// @audit `shareData[id]` is also accessed on line 124, 125
123:         shareData[id].bondingCurve = _bondingCurve;

/// @audit `shareData[_id]` is also accessed on line 135
134:         address bondingCurve = shareData[_id].bondingCurve;

/// @audit `shareData[_id]` is also accessed on line 144
143:         address bondingCurve = shareData[_id].bondingCurve;

/// @audit `shareData[_id]` is also accessed on line 159, 161, 162, 151
158:         _splitFees(_id, fee, shareData[_id].tokensInCirculation);

/// @audit `shareData[_id]` is also accessed on line 180, 182, 183
177:         _splitFees(_id, fee, shareData[_id].tokensInCirculation);

/// @audit `shareData[_id]` is also accessed on line 196
195:         address bondingCurve = shareData[_id].bondingCurve;

/// @audit `shareData[_id]` is also accessed on line 210, 212
207:         _splitFees(_id, fee, shareData[_id].tokensInCirculation);

/// @audit `shareData[_id]` is also accessed on line 233, 235
230:         _splitFees(_id, fee, shareData[_id].tokensInCirculation);

/// @audit `shareData[_id]` is also accessed on line 256, 254
255:         uint256 amount = shareData[_id].shareCreatorPool;

/// @audit `shareData[_id]` is also accessed on line 290
288:         shareData[_id].shareCreatorPool += shareCreatorFee;

/// @audit `whitelistedShareCreators[_address]` is also accessed on line 310
311:         whitelistedShareCreators[_address] = _isWhitelisted;
```


*GitHub* : [288](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L288),[106](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L106),[122](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L122),[123](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L123),[134](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L134),[143](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L143),[158](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L158),[177](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L177),[195](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L195),[207](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L207),[230](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L230),[255](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L255),[311](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L311)
### [G&#x2011;30]<a name="G-30"></a> Multiple mappings can be replaced with a single struct mapping
Saves a storage slot for the mapping. Depending on the circumstances and sizes of types, can avoid a Gsset (**20000 gas**) per mapping combined. Reads and subsequent writes can also be cheaper when a function requires both values and they both fit in the same storage slot. Finally, if both fields are accessed in the same function, can save **~42 gas per access** due to [not having to recalculate the key's keccak256 hash](https://gist.github.com/IllIllI000/ec23a57daa30a8f8ca8b9681c8ccefb0) (Gkeccak256 - 30 gas) and that calculation's associated stack operations.

*There are 4 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}43:     mapping(uint256 => ShareData) public shareData;

46:     mapping(uint256 => address) public shareBondingCurves;

52:     mapping(uint256 => mapping(address => uint256)) public tokensByAddress;

55:     mapping(uint256 => mapping(address => uint256)) public rewardsLastClaimedValue;
```


*GitHub* : [46](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L46),[43](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L43),[52](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L52),[55](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L55)### NonCritical Risk Issues


### [N&#x2011;01]<a name="N-01"></a> NatSpec documentation for contract is missing
e.g. `@dev` or `@notice`, and it must appear above the contract definition braces in order to be identified by the compiler as NatSpec.

*There are 4 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}10: contract Market is ERC1155, Ownable2Step {
```


*GitHub* : [10](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L10)

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}6: contract LinearBondingCurve is IBondingCurve {
```


*GitHub* : [6](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L6)

```solidity
File: asD/src/asD.sol

}11: contract asD is ERC20, Ownable2Step {
```


*GitHub* : [11](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L11)

```solidity
File: asD/src/asDFactory.sol

}8: contract asDFactory is Ownable2Step {
```


*GitHub* : [8](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L8)
### [N&#x2011;02]<a name="N-02"></a> Names of `private`/`internal` functions should be prefixed with an underscore
It is recommended by the [Solidity Style Guide](https://docs.soliditylang.org/en/v0.8.20/style-guide.html#underscore-prefix-for-non-external-functions-and-variables).

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}42:     function log2(uint256 x) internal pure returns (uint256 r) {
```


*GitHub* : [42](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L42)
### [N&#x2011;03]<a name="N-03"></a> Order of functions does not follow the Solidity Style Guide
According to the [Solidity Style Guide](https://docs.soliditylang.org/en/v0.8.20/style-guide.html#order-of-functions), functions should be grouped according to their visibility and ordered: `constructor`, `receive`, `fallback`, `external`, `public`, `internal`, `private`. Within a grouping, place the view and pure functions last.

*There are 13 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}/// @audit ↓↓ Out of order with `buy()`
141:     function getSellPrice(uint256 _id, uint256 _amount) public view returns (uint256 price, uint256 fee) {

/// @audit ↑↑ Out of order with `getSellPrice()`
150:     function buy(uint256 _id, uint256 _amount) external {

/// @audit ↑↑ Out of order with `buy()`
174:     function sell(uint256 _id, uint256 _amount) external {

/// @audit ↓↓ Out of order with `mintNFT()`
194:     function getNFTMintingPrice(uint256 _id, uint256 _amount) public view returns (uint256 fee) {

/// @audit ↑↑ Out of order with `getNFTMintingPrice()`
203:     function mintNFT(uint256 _id, uint256 _amount) external {

/// @audit ↑↑ Out of order with `mintNFT()`
226:     function burnNFT(uint256 _id, uint256 _amount) external {

/// @audit ↑↑ Out of order with `burnNFT()`
244:     function claimPlatformFee() external onlyOwner {

/// @audit ↑↑ Out of order with `claimPlatformFee()`
253:     function claimCreatorFee(uint256 _id) external {

/// @audit ↑↑ Out of order with `claimCreatorFee()`
263:     function claimHolderFee(uint256 _id) external {

/// @audit ↓↓ Out of order with `_splitFees()`
272:     function _getRewardsSinceLastClaim(uint256 _id) internal view returns (uint256 amount) {

/// @audit ↑↑ Out of order with `_getRewardsSinceLastClaim()`
280:     function _splitFees(
281:         uint256 _id,
282:         uint256 _fee,
283:         uint256 _tokenCount
284:     ) internal {

/// @audit ↑↑ Out of order with `_splitFees()`
300:     function restrictShareCreation(bool _isRestricted) external onlyOwner {

/// @audit ↑↑ Out of order with `restrictShareCreation()`
309:     function changeShareCreatorWhitelist(address _address, bool _isWhitelisted) external onlyOwner {
```


*GitHub* : [253](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L253),[141](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L141),[150](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L150),[174](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L174),[194](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L194),[203](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L203),[226](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L226),[244](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L244),[263](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L263),[272](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L272),[280-284](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L280-L284),[300](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L300),[309](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L309)
### [N&#x2011;04]<a name="N-04"></a> Use of `override` is unnecessary
[Starting from Solidity 0.8.8](https://docs.soliditylang.org/en/v0.8.20/contracts.html#function-overriding), the override keyword is not required when overriding an interface function, except for the case where the function is defined in multiple bases.

*There are 2 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}14:     function getPriceAndFee(uint256 shareCount, uint256 amount)
15:         external
16:         view
17:         override
18:         returns (uint256 price, uint256 fee)

27:     function getFee(uint256 shareCount) public pure override returns (uint256) {
```


*GitHub* : [14-18](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L14-L18),[27](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L27)
### [N&#x2011;05]<a name="N-05"></a> Custom errors should be used rather than `revert()`/`require()`
Custom errors are available from solidity version 0.8.4. Custom errors are more easily processed in try-catch blocks, and are easier to re-use and maintain.

*There are 12 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}81:         require(
82:             !shareCreationRestricted || whitelistedShareCreators[msg.sender] || msg.sender == owner(),
83:             "Not allowed"
84:         );

105:         require(whitelistedBondingCurves[_bondingCurve] != _newState, "State already set");

119:         require(whitelistedBondingCurves[_bondingCurve], "Bonding curve not whitelisted");

120:         require(shareIDs[_shareName] == 0, "Share already exists");

151:         require(shareData[_id].creator != msg.sender, "Creator cannot buy");

254:         require(shareData[_id].creator == msg.sender, "Not creator");

301:         require(shareCreationRestricted != _isRestricted, "State already set");

310:         require(whitelistedShareCreators[_address] != _isWhitelisted, "State already set");
```


*GitHub* : [81-84](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L81-L84),[105](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L105),[119](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L119),[120](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L120),[151](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L151),[254](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L254),[301](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L301),[310](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L310)

```solidity
File: asD/src/asD.sol

}54:         require(returnCode == 0, "Error when minting");

64:         require(returnCode == 0, "Error when redeeming"); // 0 on success: https://docs.compound.finance/v2/ctokens/#redeem-underlying

81:             require(_amount <= maximumWithdrawable, "Too many tokens requested");

86:         require(returnCode == 0, "Error when redeeming"); // 0 on success: https://docs.compound.finance/v2/ctokens/#redeem
```


*GitHub* : [54](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L54),[64](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L64),[81](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L81),[86](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L86)
### [N&#x2011;06]<a name="N-06"></a> Large numeric literals should use underscores for readability
Large hardcoded numbers in code can be difficult to read. Consider using underscores for number literals to improve readability (e.g `1234567` -> `1_234_567`). Consider using an underscore for every third digit from the right.

*There are 6 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}93:         if (block.chainid == 7700 || block.chainid == 7701) {

93:         if (block.chainid == 7700 || block.chainid == 7701) {
```


*GitHub* : [93](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L93),[93](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L93)

```solidity
File: asD/src/asD.sol

}37:         if (block.chainid == 7700 || block.chainid == 7701) {

37:         if (block.chainid == 7700 || block.chainid == 7701) {
```


*GitHub* : [37](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L37),[37](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L37)

```solidity
File: asD/src/asDFactory.sol

}26:         if (block.chainid == 7700 || block.chainid == 7701) {

26:         if (block.chainid == 7700 || block.chainid == 7701) {
```


*GitHub* : [26](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L26),[26](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L26)
### [N&#x2011;07]<a name="N-07"></a> Assembly blocks should have extensive comments
Assembly blocks take a lot more time to audit than normal Solidity code, and often have gotchas and side-effects that the Solidity versions of the same code do not. Consider adding more comments explaining what is being done in every step of the assembly code, and describe why assembly is being used instead of Solidity.

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}44:         assembly {
```


*GitHub* : [44](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L44)
### [N&#x2011;08]<a name="N-08"></a> Simplify complex require statements
Simplifying complex `require` statements with local variables and `if`(or `revert`) statements can improve readability, make debugging easier, and promote modularity and reusability in the code.

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}81:         require(
82:             !shareCreationRestricted || whitelistedShareCreators[msg.sender] || msg.sender == owner(),
83:             "Not allowed"
84:         );
```


*GitHub* : [81-84](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L81-L84)
### [N&#x2011;09]<a name="N-09"></a> Consider moving `msg.sender` checks to `modifier`s
If some functions are only allowed to be called by some specific users, consider using a modifier instead of checking with a require statement, especially if this check is done in multiple functions.

*There are 2 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}151:         require(shareData[_id].creator != msg.sender, "Creator cannot buy");

254:         require(shareData[_id].creator == msg.sender, "Not creator");
```


*GitHub* : [151](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L151),[254](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L254)
### [N&#x2011;10]<a name="N-10"></a> Consider adding a block/deny-list
Doing so will significantly increase centralization, but will help to prevent hackers from using stolen tokens

*There are 2 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}10: contract Market is ERC1155, Ownable2Step {
```


*GitHub* : [10](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L10)

```solidity
File: asD/src/asD.sol

}11: contract asD is ERC20, Ownable2Step {
```


*GitHub* : [11](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L11)
### [N&#x2011;11]<a name="N-11"></a> Constants/Immutables redefined elsewhere
Consider defining in only one contract so that values cannot become out of sync when only one location is updated. A [cheap way](https://medium.com/coinmonks/gas-cost-of-solidity-library-functions-dbe0cedd4678) to store constants/immutables in a single location is to create an `internal constant` in a `library`. If the variable is a local cache of another contract's value, consider making the cache variable internal or private, which will require external users to query the contract with the source of truth, so that callers don't get out of sync.

*There are 2 instance(s) of this issue:*

```solidity
File: asD/src/asD.sol

}/// @audit Seen in asD/src/asDFactory.sol#12
15:     address public immutable cNote; // Reference to the cNOTE token
```


*GitHub* : [15](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L15)

```solidity
File: asD/src/asDFactory.sol

}/// @audit Seen in asD/src/asD.sol#15
12:     address public immutable cNote;
```


*GitHub* : [12](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L12)
### [N&#x2011;12]<a name="N-12"></a> Convert simple `if`-statements to ternary expressions
Converting some if statements to ternaries (such as `z = (a < b) ? x : y`) can make the code more concise and easier to read.

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}29:         if (shareCount > 1) {
30:             divisor = log2(shareCount);
31:         } else {
32:             divisor = 1;
33:         }
```


*GitHub* : [29-33](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L29-L33)
### [N&#x2011;13]<a name="N-13"></a> Events should be emitted before external calls
Ensure that events follow the best practice of check-effects-interaction, and are emitted before external calls.

*There are 8 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}/// @audit `safeTransferFrom()` is called on line 153
168:         emit SharesBought(_id, msg.sender, _amount, price, fee);

/// @audit `safeTransfer()` is called on line 187
188:         emit SharesSold(_id, msg.sender, _amount, price, fee);

/// @audit `safeTransferFrom()` is called on line 206
220:         emit NFTsCreated(_id, msg.sender, _amount, fee);

/// @audit `safeTransferFrom()` is called on line 229
240:         emit NFTsBurned(_id, msg.sender, _amount, fee);

/// @audit `safeTransfer()` is called on line 247
248:         emit PlatformFeeClaimed(msg.sender, amount);

/// @audit `safeTransfer()` is called on line 257
258:         emit CreatorFeeClaimed(msg.sender, _id, amount);

/// @audit `safeTransfer()` is called on line 267
269:         emit HolderFeeClaimed(msg.sender, _id, amount);
```


*GitHub* : [188](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L188),[168](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L168),[220](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L220),[240](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L240),[248](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L248),[258](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L258),[269](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L269)

```solidity
File: asD/src/asD.sol

}/// @audit `exchangeRateCurrent()` is called on line 73
89:         emit CarryWithdrawal(_amount);
```


*GitHub* : [89](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L89)
### [N&#x2011;14]<a name="N-14"></a> Events are emitted without the sender information
When an action is triggered based on a user's action, not being able to filter based on who triggered the action makes event processing a lot more cumbersome. Including the `msg.sender` the events of these types of action will make events much more useful to end users, especially when `msg.sender` is not `tx.origin`.

*There are 3 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}107:         emit BondingCurveStateChange(_bondingCurve, _newState);

303:         emit ShareCreationRestricted(_isRestricted);
```


*GitHub* : [107](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L107),[303](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L303)

```solidity
File: asD/src/asD.sol

}89:         emit CarryWithdrawal(_amount);
```


*GitHub* : [89](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L89)
### [N&#x2011;15]<a name="N-15"></a> Event is missing `indexed` fields
Index event fields makes the field more quickly accessible to [off-chain tools](https://ethereum.stackexchange.com/questions/40396/can-somebody-please-explain-the-concept-of-event-indexing) that parse events. However, note that each indexed field costs extra gas during emission, so it's not necessarily best to index the maximum allowed per event (three fields). Each event should use three indexed fields if there are three or more fields, and gas usage is not particularly of concern for the events in question. If there are fewer than three fields, all of the fields should be indexed.

*There are 3 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}69:     event BondingCurveStateChange(address indexed curve, bool isWhitelisted);

78:     event ShareCreationRestricted(bool isRestricted);
```


*GitHub* : [69](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L69),[78](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L78)

```solidity
File: asD/src/asDFactory.sol

}20:     event CreatedToken(address token, string symbol, string name, address creator);
```


*GitHub* : [20](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L20)
### [N&#x2011;16]<a name="N-16"></a> Imports could be organized more systematically
The contract's interface should be imported first, followed by each of the interfaces it uses, followed by all other files. The examples below do not follow this layout.

*There are 4 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}/// @audit Out of order with the prev import️ ⬆
5: import {SafeERC20, IERC20} from "@openzeppelin/contracts/token/ERC20/utils/SafeERC20.sol";

/// @audit Out of order with the prev import️ ⬆
7: import {IBondingCurve} from "../interface/IBondingCurve.sol";
```


*GitHub* : [5](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L5),[7](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L7)

```solidity
File: asD/src/asD.sol

}/// @audit Out of order with the prev import️ ⬆
6: import {CTokenInterface, CErc20Interface} from "../interface/clm/CTokenInterfaces.sol";

/// @audit Out of order with the prev import️ ⬆
8: import {IERC20, ERC20} from "@openzeppelin/contracts/token/ERC20/ERC20.sol";
```


*GitHub* : [6](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L6),[8](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L8)
### [N&#x2011;17]<a name="N-17"></a> @openzeppelin/contracts should be upgraded to a newer version
These contracts import contracts from `@openzeppelin/contracts`, but they are not using [the latest version](https://github.com/OpenZeppelin/openzeppelin-contracts/releases).

The imported version is `4.9.0`.

*There are 6 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}4: import {ERC1155} from "@openzeppelin/contracts/token/ERC1155/ERC1155.sol";

4: import {ERC1155} from "@openzeppelin/contracts/token/ERC1155/ERC1155.sol";
```


*GitHub* : [4](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L4),[4](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L4)

```solidity
File: asD/src/asD.sol

}7: import {Ownable2Step} from "@openzeppelin/contracts/access/Ownable2Step.sol";

7: import {Ownable2Step} from "@openzeppelin/contracts/access/Ownable2Step.sol";
```


*GitHub* : [7](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L7),[7](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L7)

```solidity
File: asD/src/asDFactory.sol

}5: import {Ownable2Step} from "@openzeppelin/contracts/access/Ownable2Step.sol";

5: import {Ownable2Step} from "@openzeppelin/contracts/access/Ownable2Step.sol";
```


*GitHub* : [5](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L5),[5](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L5)
### [N&#x2011;18]<a name="N-18"></a> Lines are too long
The [solidity style guide](https://docs.soliditylang.org/en/v0.8.17/style-guide.html#maximum-line-length) recommends a maximum line length of 120 characters. Lines of code that are longer than 120 should be wrapped.

*There are 11 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}34:         uint256 tokensInCirculation; // Number of outstanding tokens - tokens that are minted as NFT, i.e. the number of tokens that receive fees

35:         uint256 shareHolderRewardsPerTokenScaled; // Accrued funds for the share holder per token, multiplied by 1e18 to avoid precision loss

155:         // The rewardsLastClaimedValue then needs to be updated with the new value such that the user cannot claim fees of this buy

231:         // The user does not get the proportional rewards for the burning (unless they have additional tokens that are not in the NFT)
```


*GitHub* : [155](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L155),[34](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L34),[35](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L35),[231](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L231)

```solidity
File: asD/src/asD.sol

}64:         require(returnCode == 0, "Error when redeeming"); // 0 on success: https://docs.compound.finance/v2/ctokens/#redeem-underlying

71:     /// @dev The function checks that the owner does not withdraw too much NOTE, i.e. that a 1:1 NOTE:asD exchange rate can be maintained after the withdrawal

73:         uint256 exchangeRate = CTokenInterface(cNote).exchangeRateCurrent(); // Scaled by 1 * 10^(18 - 8 + Underlying Token Decimals), i.e. 10^(28) in our case

74:         // The amount of cNOTE the contract has to hold (based on the current exchange rate which is always increasing) such that it is always possible to receive 1 NOTE when burning 1 asD

84:         // But we do not handle this case specifically, as the only consequence is that the owner wastes a bit of gas when there is nothing to withdraw

86:         require(returnCode == 0, "Error when redeeming"); // 0 on success: https://docs.compound.finance/v2/ctokens/#redeem
```


*GitHub* : [86](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L86),[64](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L64),[71](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L71),[73](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L73),[74](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L74),[84](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L84)

```solidity
File: asD/src/asDFactory.sol

}14:     /// @notice Stores the addresses of all created tokens, allowing third-party contracts to check if an address is a legit token
```


*GitHub* : [14](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L14)
### [N&#x2011;19]<a name="N-19"></a> Magic numbers should be replaced with constants
Magic numbers are hard-coded values in code that can make it difficult for developers and maintainers to understand the code, and can also cause confusion or errors. To improve the readability and maintainability of code, it is recommended to replace magic numbers with constants that have good readability.

*There are 14 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}/// @audit 7700
/// @audit 7701
93:         if (block.chainid == 7700 || block.chainid == 7701) {

/// @audit 0xEcf044C5B4b867CFda001101c617eCd347095B44
95:             Turnstile turnstile = Turnstile(0xEcf044C5B4b867CFda001101c617eCd347095B44);

/// @audit 10_000
197:         fee = (priceForOne * _amount * NFT_FEE_BPS) / 10_000;

/// @audit 1e18
276:             1e18;

/// @audit 10_000
285:         uint256 shareHolderFee = (_fee * HOLDER_CUT_BPS) / 10_000;

/// @audit 10_000
286:         uint256 shareCreatorFee = (_fee * CREATOR_CUT_BPS) / 10_000;

/// @audit 1e18
290:             shareData[_id].shareHolderRewardsPerTokenScaled += (shareHolderFee * 1e18) / _tokenCount;
```


*GitHub* : [286](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L286),[93](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L93),[95](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L95),[197](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L197),[276](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L276),[285](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L285),[290](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L290)

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}/// @audit 1e18
23:             fee += (getFee(i) * tokenPrice) / 1e18;

/// @audit 1e17
35:         return 1e17 / divisor;
```


*GitHub* : [23](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L23),[35](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L35)

```solidity
File: asD/src/asD.sol

}/// @audit 7700
/// @audit 7701
37:         if (block.chainid == 7700 || block.chainid == 7701) {

/// @audit 0xEcf044C5B4b867CFda001101c617eCd347095B44
39:             Turnstile turnstile = Turnstile(0xEcf044C5B4b867CFda001101c617eCd347095B44);

/// @audit 1e28
76:             1e28 -
```


*GitHub* : [37](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L37),[39](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L39),[76](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L76)

```solidity
File: asD/src/asDFactory.sol

}/// @audit 7700
/// @audit 7701
26:         if (block.chainid == 7700 || block.chainid == 7701) {

/// @audit 0xEcf044C5B4b867CFda001101c617eCd347095B44
28:             Turnstile turnstile = Turnstile(0xEcf044C5B4b867CFda001101c617eCd347095B44);
```


*GitHub* : [26](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L26),[28](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L28)
### [N&#x2011;20]<a name="N-20"></a> Memory-safe annotation preferred over comment variant
The memory-safe annotation (`assembly ("memory-safe") { ... }`) is preferred over the comment variant, which will be removed in a future breaking [release](https://docs.soliditylang.org/en/v0.8.13/assembly.html#memory-safety).

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}43:         /// @solidity memory-safe-assembly
```


*GitHub* : [43](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L43)
### [N&#x2011;21]<a name="N-21"></a> Use `@inheritdoc` for overridden functions
It is recommended to use `@inheritdoc` for overridden functions.

*There are 2 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}14:     function getPriceAndFee(uint256 shareCount, uint256 amount)
15:         external
16:         view
17:         override
18:         returns (uint256 price, uint256 fee)

27:     function getFee(uint256 shareCount) public pure override returns (uint256) {
```


*GitHub* : [14-18](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L14-L18),[27](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L27)
### [N&#x2011;22]<a name="N-22"></a> Contracts should have NatSpec `@author` tags
Contracts should have NatSpec `@author` tags

*There are 4 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}10: contract Market is ERC1155, Ownable2Step {
```


*GitHub* : [10](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L10)

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}6: contract LinearBondingCurve is IBondingCurve {
```


*GitHub* : [6](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L6)

```solidity
File: asD/src/asD.sol

}11: contract asD is ERC20, Ownable2Step {
```


*GitHub* : [11](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L11)

```solidity
File: asD/src/asDFactory.sol

}8: contract asDFactory is Ownable2Step {
```


*GitHub* : [8](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L8)
### [N&#x2011;23]<a name="N-23"></a> Contracts should have `@notice` tags
The `@notice` is used to explain to users what the contract does. The compiler interprets `///` or `/**` comments [as this tag](https://docs.soliditylang.org/en/latest/natspec-format.html#tags) if one wasn't explicitly provided.

*There are 4 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}10: contract Market is ERC1155, Ownable2Step {
```


*GitHub* : [10](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L10)

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}6: contract LinearBondingCurve is IBondingCurve {
```


*GitHub* : [6](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L6)

```solidity
File: asD/src/asD.sol

}11: contract asD is ERC20, Ownable2Step {
```


*GitHub* : [11](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L11)

```solidity
File: asD/src/asDFactory.sol

}8: contract asDFactory is Ownable2Step {
```


*GitHub* : [8](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L8)
### [N&#x2011;24]<a name="N-24"></a> Contracts should have NatSpec `@title` tags
Some contract definitions have an incomplete NatSpec: add a `@title` notation to describe the contract to improve the code documentation.

*There are 4 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}10: contract Market is ERC1155, Ownable2Step {
```


*GitHub* : [10](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L10)

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}6: contract LinearBondingCurve is IBondingCurve {
```


*GitHub* : [6](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L6)

```solidity
File: asD/src/asD.sol

}11: contract asD is ERC20, Ownable2Step {
```


*GitHub* : [11](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L11)

```solidity
File: asD/src/asDFactory.sol

}8: contract asDFactory is Ownable2Step {
```


*GitHub* : [8](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L8)
### [N&#x2011;25]<a name="N-25"></a> Events missing NatSpec `@param` tag
Each modifier parameter should have a `@param` notation to improve the code documentation.

*There are 12 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}/// @audit Missing @param for `curve`, `isWhitelisted`
69:     event BondingCurveStateChange(address indexed curve, bool isWhitelisted);

/// @audit Missing @param for `id`, `name`, `bondingCurve`, `creator`
70:     event ShareCreated(uint256 indexed id, string name, address indexed bondingCurve, address indexed creator);

/// @audit Missing @param for `id`, `buyer`, `amount`, `price`, `fee`
71:     event SharesBought(uint256 indexed id, address indexed buyer, uint256 amount, uint256 price, uint256 fee);

/// @audit Missing @param for `id`, `seller`, `amount`, `price`, `fee`
72:     event SharesSold(uint256 indexed id, address indexed seller, uint256 amount, uint256 price, uint256 fee);

/// @audit Missing @param for `id`, `creator`, `amount`, `fee`
73:     event NFTsCreated(uint256 indexed id, address indexed creator, uint256 amount, uint256 fee);

/// @audit Missing @param for `id`, `burner`, `amount`, `fee`
74:     event NFTsBurned(uint256 indexed id, address indexed burner, uint256 amount, uint256 fee);

/// @audit Missing @param for `claimer`, `amount`
75:     event PlatformFeeClaimed(address indexed claimer, uint256 amount);

/// @audit Missing @param for `claimer`, `id`, `amount`
76:     event CreatorFeeClaimed(address indexed claimer, uint256 indexed id, uint256 amount);

/// @audit Missing @param for `claimer`, `id`, `amount`
77:     event HolderFeeClaimed(address indexed claimer, uint256 indexed id, uint256 amount);

/// @audit Missing @param for `isRestricted`
78:     event ShareCreationRestricted(bool isRestricted);
```


*GitHub* : [77](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L77),[76](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L76),[75](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L75),[74](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L74),[78](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L78),[72](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L72),[73](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L73),[69](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L69),[70](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L70),[71](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L71)

```solidity
File: asD/src/asD.sol

}/// @audit Missing @param for `amount`
20:     event CarryWithdrawal(uint256 amount);
```


*GitHub* : [20](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L20)

```solidity
File: asD/src/asDFactory.sol

}/// @audit Missing @param for `token`, `symbol`, `name`, `creator`
20:     event CreatedToken(address token, string symbol, string name, address creator);
```


*GitHub* : [20](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L20)
### [N&#x2011;26]<a name="N-26"></a> Event declarations should have NatSpec descriptions
Event declarations should have NatSpec descriptions

*There are 12 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}69:     event BondingCurveStateChange(address indexed curve, bool isWhitelisted);

70:     event ShareCreated(uint256 indexed id, string name, address indexed bondingCurve, address indexed creator);

71:     event SharesBought(uint256 indexed id, address indexed buyer, uint256 amount, uint256 price, uint256 fee);

72:     event SharesSold(uint256 indexed id, address indexed seller, uint256 amount, uint256 price, uint256 fee);

73:     event NFTsCreated(uint256 indexed id, address indexed creator, uint256 amount, uint256 fee);

74:     event NFTsBurned(uint256 indexed id, address indexed burner, uint256 amount, uint256 fee);

75:     event PlatformFeeClaimed(address indexed claimer, uint256 amount);

76:     event CreatorFeeClaimed(address indexed claimer, uint256 indexed id, uint256 amount);

77:     event HolderFeeClaimed(address indexed claimer, uint256 indexed id, uint256 amount);

78:     event ShareCreationRestricted(bool isRestricted);
```


*GitHub* : [74](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L74),[69](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L69),[70](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L70),[71](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L71),[72](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L72),[73](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L73),[75](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L75),[76](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L76),[77](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L77),[78](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L78)

```solidity
File: asD/src/asD.sol

}20:     event CarryWithdrawal(uint256 amount);
```


*GitHub* : [20](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L20)

```solidity
File: asD/src/asDFactory.sol

}20:     event CreatedToken(address token, string symbol, string name, address creator);
```


*GitHub* : [20](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L20)
### [N&#x2011;27]<a name="N-27"></a> Functions missing NatSpec `@param` tag
Each function parameter should have a `@param` notation to improve the code documentation.

*There are 7 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}/// @audit Missing @param for `_id`
272:     function _getRewardsSinceLastClaim(uint256 _id) internal view returns (uint256 amount) {

/// @audit Missing @param for `_id`, `_fee`, `_tokenCount`
280:     function _splitFees(
281:         uint256 _id,
282:         uint256 _fee,
283:         uint256 _tokenCount
284:     ) internal {
```


*GitHub* : [272](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L272),[280-284](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L280-L284)

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}/// @audit Missing @param for `_priceIncrease`
10:     constructor(uint256 _priceIncrease) {

/// @audit Missing @param for `shareCount`, `amount`
14:     function getPriceAndFee(uint256 shareCount, uint256 amount)

/// @audit Missing @param for `shareCount`
27:     function getFee(uint256 shareCount) public pure override returns (uint256) {

/// @audit Missing @param for `x`
42:     function log2(uint256 x) internal pure returns (uint256 r) {
```


*GitHub* : [42](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L42),[27](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L27),[10](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L10),[14](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L14)

```solidity
File: asD/src/asDFactory.sol

}/// @audit Missing @param for `_name`, `_symbol`
33:     function create(string memory _name, string memory _symbol) external returns (address) {
```


*GitHub* : [33](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L33)
### [N&#x2011;28]<a name="N-28"></a> NatSpec documentation for function is missing
It is recommended that Solidity contracts are fully annotated using NatSpec for all public interfaces (everything in the ABI). It is clearly stated in the Solidity official documentation.
In complex projects such as DeFi, the interpretation of all functions and their arguments and returns is important for code readability and auditability.

*There are 5 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}272:     function _getRewardsSinceLastClaim(uint256 _id) internal view returns (uint256 amount) {
```


*GitHub* : [272](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L272)

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}10:     constructor(uint256 _priceIncrease) {

14:     function getPriceAndFee(uint256 shareCount, uint256 amount)

27:     function getFee(uint256 shareCount) public pure override returns (uint256) {
```


*GitHub* : [10](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L10),[14](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L14),[27](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L27)

```solidity
File: asD/src/asDFactory.sol

}33:     function create(string memory _name, string memory _symbol) external returns (address) {
```


*GitHub* : [33](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L33)
### [N&#x2011;29]<a name="N-29"></a> Functions missing NatSpec `@return` tag
Functions missing NatSpec `@return` tag

*There are 9 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}114:     function createNewShare(
115:         string memory _shareName,
116:         address _bondingCurve,
117:         string memory _metadataURI
118:     ) external onlyShareCreator returns (uint256 id) {

132:     function getBuyPrice(uint256 _id, uint256 _amount) public view returns (uint256 price, uint256 fee) {

141:     function getSellPrice(uint256 _id, uint256 _amount) public view returns (uint256 price, uint256 fee) {

194:     function getNFTMintingPrice(uint256 _id, uint256 _amount) public view returns (uint256 fee) {

272:     function _getRewardsSinceLastClaim(uint256 _id) internal view returns (uint256 amount) {
```


*GitHub* : [114-118](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L114-L118),[272](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L272),[194](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L194),[141](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L141),[132](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L132)

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}14:     function getPriceAndFee(uint256 shareCount, uint256 amount)
15:         external
16:         view
17:         override
18:         returns (uint256 price, uint256 fee)

27:     function getFee(uint256 shareCount) public pure override returns (uint256) {

42:     function log2(uint256 x) internal pure returns (uint256 r) {
```


*GitHub* : [27](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L27),[42](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L42),[14-18](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L14-L18)

```solidity
File: asD/src/asDFactory.sol

}33:     function create(string memory _name, string memory _symbol) external returns (address) {
```


*GitHub* : [33](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L33)
### [N&#x2011;30]<a name="N-30"></a> State variables should have NatSpec descriptions
It is [recommended](https://docs.soliditylang.org/en/v0.8.20/natspec-format.html#tags) to use the NatSpec tags `@notice`, `@dev`, `@return`, `@inheritdoc` for public state variables, and `@dev` for non-public state variables.

*There are 6 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}14:     uint256 public constant NFT_FEE_BPS = 1_000; // 10%

15:     uint256 public constant HOLDER_CUT_BPS = 3_300; // 33%

16:     uint256 public constant CREATOR_CUT_BPS = 3_300; // 33%
```


*GitHub* : [14](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L14),[16](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L16),[15](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L15)

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}8:     uint256 public immutable priceIncrease;
```


*GitHub* : [8](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L8)

```solidity
File: asD/src/asD.sol

}15:     address public immutable cNote; // Reference to the cNOTE token
```


*GitHub* : [15](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L15)

```solidity
File: asD/src/asDFactory.sol

}12:     address public immutable cNote;
```


*GitHub* : [12](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L12)
### [N&#x2011;31]<a name="N-31"></a> Contract name does not follow the Solidity Style Guide
According to the [Solidity Style Guide](https://docs.soliditylang.org/en/latest/style-guide.html#contract-and-library-names), contracts and libraries should be named using the CapWords style.

*There are 2 instance(s) of this issue:*

```solidity
File: asD/src/asD.sol

}11: contract asD is ERC20, Ownable2Step {
```


*GitHub* : [11](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L11)

```solidity
File: asD/src/asDFactory.sol

}8: contract asDFactory is Ownable2Step {
```


*GitHub* : [8](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L8)
### [N&#x2011;32]<a name="N-32"></a> Functions should be named in mixedCase style
As the [Solidity Style Guide](https://docs.soliditylang.org/en/v0.8.21/style-guide.html#function-names) suggests: functions should be named in mixedCase style.

*There are 3 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}194:     function getNFTMintingPrice(uint256 _id, uint256 _amount) public view returns (uint256 fee) {

203:     function mintNFT(uint256 _id, uint256 _amount) external {

226:     function burnNFT(uint256 _id, uint256 _amount) external {
```


*GitHub* : [194](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L194),[226](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L226),[203](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L203)
### [N&#x2011;33]<a name="N-33"></a> Variable names for `immutable`s should use UPPER_CASE_WITH_UNDERSCORES
For `immutable` variable names, each word should use all capital letters, with underscores separating each word (UPPER_CASE_WITH_UNDERSCORES)

*There are 4 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}20:     IERC20 public immutable token;
```


*GitHub* : [20](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L20)

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}8:     uint256 public immutable priceIncrease;
```


*GitHub* : [8](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L8)

```solidity
File: asD/src/asD.sol

}15:     address public immutable cNote; // Reference to the cNOTE token
```


*GitHub* : [15](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L15)

```solidity
File: asD/src/asDFactory.sol

}12:     address public immutable cNote;
```


*GitHub* : [12](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L12)
### [N&#x2011;34]<a name="N-34"></a> Missing zero address check in functions with address parameters
Adding a zero address check for each address type parameter can prevent errors.

*There are 3 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}/// @audit `_bondingCurve not checked`
104:     function changeBondingCurveAllowed(address _bondingCurve, bool _newState) external onlyOwner {

/// @audit `_bondingCurve not checked`
114:     function createNewShare(
115:         string memory _shareName,
116:         address _bondingCurve,
117:         string memory _metadataURI
118:     ) external onlyShareCreator returns (uint256 id) {

/// @audit `_address not checked`
309:     function changeShareCreatorWhitelist(address _address, bool _isWhitelisted) external onlyOwner {
```


*GitHub* : [309](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L309),[114-118](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L114-L118),[104](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L104)
### [N&#x2011;35]<a name="N-35"></a> Constants should be put on the left side of comparisons
Putting constants on the left side of comparison statements is a best practice known as [Yoda conditions](https://en.wikipedia.org/wiki/Yoda_conditions).
Although solidity's static typing system prevents accidental assignments within conditionals, adopting this practice can improve code readability and consistency, especially when working across multiple languages.

*There are 11 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}/// @audit put `7700` on the left
93:         if (block.chainid == 7700 || block.chainid == 7701) {

/// @audit put `7701` on the left
93:         if (block.chainid == 7700 || block.chainid == 7701) {

/// @audit put `0` on the left
120:         require(shareIDs[_shareName] == 0, "Share already exists");
```


*GitHub* : [120](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L120),[93](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L93),[93](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L93)

```solidity
File: asD/src/asD.sol

}/// @audit put `7700` on the left
37:         if (block.chainid == 7700 || block.chainid == 7701) {

/// @audit put `7701` on the left
37:         if (block.chainid == 7700 || block.chainid == 7701) {

/// @audit put `0` on the left
54:         require(returnCode == 0, "Error when minting");

/// @audit put `0` on the left
64:         require(returnCode == 0, "Error when redeeming"); // 0 on success: https://docs.compound.finance/v2/ctokens/#redeem-underlying

/// @audit put `0` on the left
78:         if (_amount == 0) {

/// @audit put `0` on the left
86:         require(returnCode == 0, "Error when redeeming"); // 0 on success: https://docs.compound.finance/v2/ctokens/#redeem
```


*GitHub* : [78](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L78),[37](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L37),[37](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L37),[54](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L54),[64](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L64),[86](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L86)

```solidity
File: asD/src/asDFactory.sol

}/// @audit put `7700` on the left
26:         if (block.chainid == 7700 || block.chainid == 7701) {

/// @audit put `7701` on the left
26:         if (block.chainid == 7700 || block.chainid == 7701) {
```


*GitHub* : [26](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L26),[26](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L26)
### [N&#x2011;36]<a name="N-36"></a> Large multiples of ten should use scientific notation
Use a scientific notation rather than decimal literals (e.g. `1e6` instead of `1000000`), for better code readability.

*There are 4 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}/// @audit 1_000 -> 1e3
14:     uint256 public constant NFT_FEE_BPS = 1_000; // 10%

/// @audit 10_000 -> 1e4
197:         fee = (priceForOne * _amount * NFT_FEE_BPS) / 10_000;

/// @audit 10_000 -> 1e4
285:         uint256 shareHolderFee = (_fee * HOLDER_CUT_BPS) / 10_000;

/// @audit 10_000 -> 1e4
286:         uint256 shareCreatorFee = (_fee * CREATOR_CUT_BPS) / 10_000;
```


*GitHub* : [286](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L286),[14](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L14),[197](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L197),[285](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L285)
### [N&#x2011;37]<a name="N-37"></a> Non-interface files should use fixed compiler versions
To prevent the actual contracts being deployed from behaving differently depending on the compiler version, it is recommended to use fixed solidity versions for contracts and libraries.

Although we can configure a specific version through config (like hardhat, forge config files), it is recommended to **set the fixed version in the solidity pragma directly** before deploying to the mainnet.

*There are 2 instance(s) of this issue:*

```solidity
File: asD/src/asD.sol

}2: pragma solidity >=0.8.0;
```


*GitHub* : [2](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L2)

```solidity
File: asD/src/asDFactory.sol

}2: pragma solidity >=0.8.0;
```


*GitHub* : [2](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L2)
### [N&#x2011;38]<a name="N-38"></a> Unused contract variables
The following state variables are defined but not used.
It is recommended to check the code for logical omissions that cause them not to be used. If it's determined that they are not needed anywhere, it's best to remove them from the codebase to improve code clarity and minimize confusion.

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}46:     mapping(uint256 => address) public shareBondingCurves;
```


*GitHub* : [46](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L46)
### [N&#x2011;39]<a name="N-39"></a> Unused import
The identifier is imported but never used within the file.

*There are 1 instance(s) of this issue:*

```solidity
File: asD/src/asD.sol

}/// @audit IasDFactory
5: import {IasDFactory} from "../interface/IasDFactory.sol";
```


*GitHub* : [5](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L5)
### [N&#x2011;40]<a name="N-40"></a> Consider using `delete` rather than assigning zero to clear values
The `delete` keyword more closely matches the semantics of what is being done, and draws more attention to the changing of state, which may lead to a more thorough audit of its associated logic.

*There are 2 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}246:         platformPool = 0;

256:         shareData[_id].shareCreatorPool = 0;
```


*GitHub* : [246](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L246),[256](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L256)
### [N&#x2011;41]<a name="N-41"></a> Use the latest Solidity version
Upgrading to the [latest solidity version](https://github.com/ethereum/solc-js/tags) (0.8.19 for L2s) can optimize gas usage, take advantage of new features and improve overall contract efficiency. Where possible, based on compatibility requirements, it is recommended to use newer/latest solidity version to take advantage of the latest optimizations and features.

*There are 4 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}2: pragma solidity 0.8.19;
```


*GitHub* : [2](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L2)

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}2: pragma solidity 0.8.19;
```


*GitHub* : [2](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L2)

```solidity
File: asD/src/asD.sol

}2: pragma solidity >=0.8.0;
```


*GitHub* : [2](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L2)

```solidity
File: asD/src/asDFactory.sol

}2: pragma solidity >=0.8.0;
```


*GitHub* : [2](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L2)
### [N&#x2011;42]<a name="N-42"></a> Named mappings are recommended
[Named mappings](https://docs.soliditylang.org/en/v0.8.18/types.html#mapping-types) (with syntax `mapping(KeyType KeyName? => ValueType ValueName?)`) are recommended.It can make the mapping variables clearer, more readable and easier to maintain.

*There are 10 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}30:     mapping(string => uint256) public shareIDs;

43:     mapping(uint256 => ShareData) public shareData;

46:     mapping(uint256 => address) public shareBondingCurves;

49:     mapping(address => bool) public whitelistedBondingCurves;

52:     mapping(uint256 => mapping(address => uint256)) public tokensByAddress;

52:     mapping(uint256 => mapping(address => uint256)) public tokensByAddress;

55:     mapping(uint256 => mapping(address => uint256)) public rewardsLastClaimedValue;

55:     mapping(uint256 => mapping(address => uint256)) public rewardsLastClaimedValue;

64:     mapping(address => bool) public whitelistedShareCreators;
```


*GitHub* : [55](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L55),[64](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L64),[52](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L52),[55](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L55),[52](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L52),[30](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L30),[43](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L43),[46](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L46),[49](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L49)

```solidity
File: asD/src/asDFactory.sol

}15:     mapping(address => bool) public isAsD;
```


*GitHub* : [15](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L15)
### [N&#x2011;43]<a name="N-43"></a> Whitespace in Expressions
See the [Whitespace in Expressions](https://docs.soliditylang.org/en/latest/style-guide.html#whitespace-in-expressions) section of the Solidity Style Guide.

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}/// @audit Whitespace inside parenthesis
196:         (uint256 priceForOne, ) = IBondingCurve(bondingCurve).getPriceAndFee(shareData[_id].tokenCount, 1);
```


*GitHub* : [196](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L196)
### [N&#x2011;44]<a name="N-44"></a> Modifier declarations should have NatSpec descriptions
Modifier declarations should have NatSpec descriptions

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}80:     modifier onlyShareCreator() {
```


*GitHub* : [80](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L80)
### [N&#x2011;45]<a name="N-45"></a> Contract functions should use an `interface`
All `external`/`public` functions should extend an `interface`. This is useful to ensure that the whole API is extracted and can be more easily integrated by other projects.

*There are 18 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}104:     function changeBondingCurveAllowed(address _bondingCurve, bool _newState) external onlyOwner {

114:     function createNewShare(
115:         string memory _shareName,
116:         address _bondingCurve,
117:         string memory _metadataURI
118:     ) external onlyShareCreator returns (uint256 id) {

132:     function getBuyPrice(uint256 _id, uint256 _amount) public view returns (uint256 price, uint256 fee) {

141:     function getSellPrice(uint256 _id, uint256 _amount) public view returns (uint256 price, uint256 fee) {

150:     function buy(uint256 _id, uint256 _amount) external {

174:     function sell(uint256 _id, uint256 _amount) external {

194:     function getNFTMintingPrice(uint256 _id, uint256 _amount) public view returns (uint256 fee) {

203:     function mintNFT(uint256 _id, uint256 _amount) external {

226:     function burnNFT(uint256 _id, uint256 _amount) external {

244:     function claimPlatformFee() external onlyOwner {

253:     function claimCreatorFee(uint256 _id) external {

263:     function claimHolderFee(uint256 _id) external {

300:     function restrictShareCreation(bool _isRestricted) external onlyOwner {

309:     function changeShareCreatorWhitelist(address _address, bool _isWhitelisted) external onlyOwner {
```


*GitHub* : [114-118](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L114-L118),[104](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L104),[132](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L132),[141](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L141),[150](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L150),[174](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L174),[194](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L194),[203](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L203),[226](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L226),[244](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L244),[253](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L253),[263](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L263),[300](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L300),[309](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L309)

```solidity
File: asD/src/asD.sol

}47:     function mint(uint256 _amount) external {

60:     function burn(uint256 _amount) external {

72:     function withdrawCarry(uint256 _amount) external onlyOwner {
```


*GitHub* : [72](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L72),[47](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L47),[60](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L60)

```solidity
File: asD/src/asDFactory.sol

}33:     function create(string memory _name, string memory _symbol) external returns (address) {
```


*GitHub* : [33](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L33)
### [N&#x2011;46]<a name="N-46"></a> Addresses shouldn't be hard-coded
It is often better to declare `address`es as `constant` or `immutable` which can be assigned in constructor. This allows the code to remain the same across deployments on different networks, and avoids recompilation when addresses need to change.

*There are 3 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}95:             Turnstile turnstile = Turnstile(0xEcf044C5B4b867CFda001101c617eCd347095B44);
```


*GitHub* : [95](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L95)

```solidity
File: asD/src/asD.sol

}39:             Turnstile turnstile = Turnstile(0xEcf044C5B4b867CFda001101c617eCd347095B44);
```


*GitHub* : [39](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L39)

```solidity
File: asD/src/asDFactory.sol

}28:             Turnstile turnstile = Turnstile(0xEcf044C5B4b867CFda001101c617eCd347095B44);
```


*GitHub* : [28](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L28)
### [N&#x2011;47]<a name="N-47"></a> Multiple mappings with same keys can be combined into a single struct mapping for readability
Well-organized data structures make code reviews easier, which may lead to fewer bugs. Consider combining related mappings into mappings to structs, so it's clear what data is related.

*There are 4 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}43:     mapping(uint256 => ShareData) public shareData;

46:     mapping(uint256 => address) public shareBondingCurves;

52:     mapping(uint256 => mapping(address => uint256)) public tokensByAddress;

55:     mapping(uint256 => mapping(address => uint256)) public rewardsLastClaimedValue;
```


*GitHub* : [55](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L55),[43](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L43),[46](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L46),[52](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L52)
### [N&#x2011;48]<a name="N-48"></a> Control structures do not follow the Solidity Style Guide
Refer to the [Solidity style guide - Control Structures](https://docs.soliditylang.org/en/v0.8.20/style-guide.html#control-structures).

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}14:     function getPriceAndFee(uint256 shareCount, uint256 amount)
15:         external
16:         view
17:         override
18:         returns (uint256 price, uint256 fee)
19:     {
```


*GitHub* : [14-19](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L14-L19)
### [N&#x2011;49]<a name="N-49"></a> Do not cache immutable variables
Instead of caching immutable variables, using them directly can make code more consistent and less prone to errors.

*There are 2 instance(s) of this issue:*

```solidity
File: asD/src/asD.sol

}48:         CErc20Interface cNoteToken = CErc20Interface(cNote);

61:         CErc20Interface cNoteToken = CErc20Interface(cNote);
```


*GitHub* : [61](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L61),[48](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L48)
### [N&#x2011;50]<a name="N-50"></a> Missing event for critical changes
Events should be emitted when critical changes are made to the contracts.

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}309:     function changeShareCreatorWhitelist(address _address, bool _isWhitelisted) external onlyOwner {
310:         require(whitelistedShareCreators[_address] != _isWhitelisted, "State already set");
311:         whitelistedShareCreators[_address] = _isWhitelisted;
312:     }
```


*GitHub* : [309-312](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L309-L312)
### [N&#x2011;51]<a name="N-51"></a> Duplicated `require()`/`revert()` checks should be refactored
Refactoring duplicate `require()`/`revert()` checks into a modifier or function can make the code more concise, readable and maintainable, and less likely to make errors or omissions when modifying the `require()` or `revert()`.

*There are 1 instance(s) of this issue:*

```solidity
File: asD/src/asD.sol

}/// @audit Duplicated on line 86
64:         require(returnCode == 0, "Error when redeeming"); // 0 on success: https://docs.compound.finance/v2/ctokens/#redeem-underlying
```


*GitHub* : [64](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L64)
### [N&#x2011;52]<a name="N-52"></a> Consider adding emergency-stop functionality
Adding a way to quickly halt protocol functionality in an emergency, rather than having to pause individual contracts one-by-one, will make in-progress hack mitigation faster and much less stressful.

*There are 3 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}10: contract Market is ERC1155, Ownable2Step {
```


*GitHub* : [10](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L10)

```solidity
File: asD/src/asD.sol

}11: contract asD is ERC20, Ownable2Step {
```


*GitHub* : [11](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L11)

```solidity
File: asD/src/asDFactory.sol

}8: contract asDFactory is Ownable2Step {
```


*GitHub* : [8](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L8)
### [N&#x2011;53]<a name="N-53"></a> Avoid the use of sensitive terms
Use [alternative variants](https://www.zdnet.com/article/mysql-drops-master-slave-and-blacklist-whitelist-terminology/), e.g. allowlist/denylist instead of whitelist/blacklist.

*There are 23 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}49:     mapping(address => bool) public whitelistedBondingCurves;

60:     /// @notice If true, only the whitelisted addresses can create shares

64:     mapping(address => bool) public whitelistedShareCreators;

69:     event BondingCurveStateChange(address indexed curve, bool isWhitelisted);

82:             !shareCreationRestricted || whitelistedShareCreators[msg.sender] || msg.sender == owner(),

100:     /// @notice Whitelist or remove whitelist for a bonding curve.

100:     /// @notice Whitelist or remove whitelist for a bonding curve.

101:     /// @dev Whitelisting status is only checked when adding a share

103:     /// @param _newState True if whitelisted, false if not

105:         require(whitelistedBondingCurves[_bondingCurve] != _newState, "State already set");

106:         whitelistedBondingCurves[_bondingCurve] = _newState;

112:     /// @param _bondingCurve Address of the bonding curve, has to be whitelisted

119:         require(whitelistedBondingCurves[_bondingCurve], "Bonding curve not whitelisted");

119:         require(whitelistedBondingCurves[_bondingCurve], "Bonding curve not whitelisted");

306:     /// @notice Adds or removes an address from the whitelist of share creators

308:     /// @param _isWhitelisted True if whitelisted, false if not

308:     /// @param _isWhitelisted True if whitelisted, false if not

309:     function changeShareCreatorWhitelist(address _address, bool _isWhitelisted) external onlyOwner {

309:     function changeShareCreatorWhitelist(address _address, bool _isWhitelisted) external onlyOwner {

310:         require(whitelistedShareCreators[_address] != _isWhitelisted, "State already set");

310:         require(whitelistedShareCreators[_address] != _isWhitelisted, "State already set");

311:         whitelistedShareCreators[_address] = _isWhitelisted;

311:         whitelistedShareCreators[_address] = _isWhitelisted;
```


*GitHub* : [101](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L101),[311](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L311),[311](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L311),[310](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L310),[310](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L310),[309](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L309),[309](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L309),[308](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L308),[308](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L308),[306](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L306),[119](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L119),[119](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L119),[112](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L112),[106](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L106),[105](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L105),[103](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L103),[100](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L100),[100](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L100),[82](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L82),[69](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L69),[64](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L64),[60](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L60),[49](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L49)
### [N&#x2011;54]<a name="N-54"></a> Contracts should have NatSpec `@dev` tags
The `@dev` tag is used to explain extra details to developers.

*There are 4 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}10: contract Market is ERC1155, Ownable2Step {
```


*GitHub* : [10](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L10)

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}6: contract LinearBondingCurve is IBondingCurve {
```


*GitHub* : [6](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L6)

```solidity
File: asD/src/asD.sol

}11: contract asD is ERC20, Ownable2Step {
```


*GitHub* : [11](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L11)

```solidity
File: asD/src/asDFactory.sol

}8: contract asDFactory is Ownable2Step {
```


*GitHub* : [8](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L8)
### [N&#x2011;55]<a name="N-55"></a> Missing NatSpec `@dev` from event declaration
Some events have an incomplete NatSpec: add a `@dev` notation to describe the event to improve the code documentation.

*There are 12 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}69:     event BondingCurveStateChange(address indexed curve, bool isWhitelisted);

70:     event ShareCreated(uint256 indexed id, string name, address indexed bondingCurve, address indexed creator);

71:     event SharesBought(uint256 indexed id, address indexed buyer, uint256 amount, uint256 price, uint256 fee);

72:     event SharesSold(uint256 indexed id, address indexed seller, uint256 amount, uint256 price, uint256 fee);

73:     event NFTsCreated(uint256 indexed id, address indexed creator, uint256 amount, uint256 fee);

74:     event NFTsBurned(uint256 indexed id, address indexed burner, uint256 amount, uint256 fee);

75:     event PlatformFeeClaimed(address indexed claimer, uint256 amount);

76:     event CreatorFeeClaimed(address indexed claimer, uint256 indexed id, uint256 amount);

77:     event HolderFeeClaimed(address indexed claimer, uint256 indexed id, uint256 amount);

78:     event ShareCreationRestricted(bool isRestricted);
```


*GitHub* : [72](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L72),[71](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L71),[70](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L70),[69](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L69),[76](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L76),[73](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L73),[74](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L74),[78](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L78),[77](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L77),[75](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L75)

```solidity
File: asD/src/asD.sol

}20:     event CarryWithdrawal(uint256 amount);
```


*GitHub* : [20](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L20)

```solidity
File: asD/src/asDFactory.sol

}20:     event CreatedToken(address token, string symbol, string name, address creator);
```


*GitHub* : [20](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L20)
### [N&#x2011;56]<a name="N-56"></a> Missing NatSpec `@notice` from event declaration
Some events have an incomplete NatSpec: add a @notice notation to describe the event to improve the code documentation.

*There are 12 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}69:     event BondingCurveStateChange(address indexed curve, bool isWhitelisted);

70:     event ShareCreated(uint256 indexed id, string name, address indexed bondingCurve, address indexed creator);

71:     event SharesBought(uint256 indexed id, address indexed buyer, uint256 amount, uint256 price, uint256 fee);

72:     event SharesSold(uint256 indexed id, address indexed seller, uint256 amount, uint256 price, uint256 fee);

73:     event NFTsCreated(uint256 indexed id, address indexed creator, uint256 amount, uint256 fee);

74:     event NFTsBurned(uint256 indexed id, address indexed burner, uint256 amount, uint256 fee);

75:     event PlatformFeeClaimed(address indexed claimer, uint256 amount);

76:     event CreatorFeeClaimed(address indexed claimer, uint256 indexed id, uint256 amount);

77:     event HolderFeeClaimed(address indexed claimer, uint256 indexed id, uint256 amount);

78:     event ShareCreationRestricted(bool isRestricted);
```


*GitHub* : [71](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L71),[69](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L69),[72](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L72),[70](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L70),[78](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L78),[77](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L77),[76](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L76),[75](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L75),[74](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L74),[73](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L73)

```solidity
File: asD/src/asD.sol

}20:     event CarryWithdrawal(uint256 amount);
```


*GitHub* : [20](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L20)

```solidity
File: asD/src/asDFactory.sol

}20:     event CreatedToken(address token, string symbol, string name, address creator);
```


*GitHub* : [20](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L20)
### [N&#x2011;57]<a name="N-57"></a> Missing NatSpec `@dev` from function declaration
Some functions have an incomplete NatSpec: add a `@dev` notation to describe the function to improve the code documentation.

*There are 23 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}91:     constructor(string memory _uri, address _paymentToken) ERC1155(_uri) Ownable() {

114:     function createNewShare(

132:     function getBuyPrice(uint256 _id, uint256 _amount) public view returns (uint256 price, uint256 fee) {

141:     function getSellPrice(uint256 _id, uint256 _amount) public view returns (uint256 price, uint256 fee) {

150:     function buy(uint256 _id, uint256 _amount) external {

174:     function sell(uint256 _id, uint256 _amount) external {

194:     function getNFTMintingPrice(uint256 _id, uint256 _amount) public view returns (uint256 fee) {

203:     function mintNFT(uint256 _id, uint256 _amount) external {

226:     function burnNFT(uint256 _id, uint256 _amount) external {

244:     function claimPlatformFee() external onlyOwner {

253:     function claimCreatorFee(uint256 _id) external {

263:     function claimHolderFee(uint256 _id) external {

272:     function _getRewardsSinceLastClaim(uint256 _id) internal view returns (uint256 amount) {

280:     function _splitFees(

300:     function restrictShareCreation(bool _isRestricted) external onlyOwner {

309:     function changeShareCreatorWhitelist(address _address, bool _isWhitelisted) external onlyOwner {
```


*GitHub* : [309](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L309),[91](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L91),[114](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L114),[132](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L132),[141](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L141),[150](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L150),[174](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L174),[194](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L194),[203](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L203),[226](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L226),[244](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L244),[253](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L253),[263](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L263),[272](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L272),[280](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L280),[300](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L300)

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}10:     constructor(uint256 _priceIncrease) {

14:     function getPriceAndFee(uint256 shareCount, uint256 amount)

27:     function getFee(uint256 shareCount) public pure override returns (uint256) {
```


*GitHub* : [10](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L10),[14](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L14),[27](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L27)

```solidity
File: asD/src/asD.sol

}28:     constructor(

60:     function burn(uint256 _amount) external {
```


*GitHub* : [28](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L28),[60](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L60)

```solidity
File: asD/src/asDFactory.sol

}24:     constructor(address _cNote) {

33:     function create(string memory _name, string memory _symbol) external returns (address) {
```


*GitHub* : [33](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L33),[24](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L24)
### [N&#x2011;58]<a name="N-58"></a> Missing NatSpec `@notice` from function declaration
Some functions have an incomplete NatSpec: add a `@notice` notation to describe the function to improve the code documentation.

*There are 5 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}272:     function _getRewardsSinceLastClaim(uint256 _id) internal view returns (uint256 amount) {
```


*GitHub* : [272](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L272)

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}10:     constructor(uint256 _priceIncrease) {

14:     function getPriceAndFee(uint256 shareCount, uint256 amount)

27:     function getFee(uint256 shareCount) public pure override returns (uint256) {
```


*GitHub* : [10](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L10),[14](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L14),[27](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L27)

```solidity
File: asD/src/asDFactory.sol

}33:     function create(string memory _name, string memory _symbol) external returns (address) {
```


*GitHub* : [33](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L33)
### [N&#x2011;59]<a name="N-59"></a> Missing NatSpec `@dev` from modifier declaration
Some modifiers have an incomplete NatSpec: add a `@dev` notation to describe the modifier to improve the code documentation.

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}80:     modifier onlyShareCreator() {
```


*GitHub* : [80](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L80)
### [N&#x2011;60]<a name="N-60"></a> Missing NatSpec `@notice` from modifier declaration
Some modifiers have an incomplete NatSpec: add a `@notice` notation to describe the modifier to improve the code documentation.

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}80:     modifier onlyShareCreator() {
```


*GitHub* : [80](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L80)
### [N&#x2011;61]<a name="N-61"></a> Contracts should have full test coverage
While 100% code coverage does not guarantee that there are no bugs, it often will catch easy-to-find bugs, and will ensure that there are fewer regressions when the code invariably has to be modified. Furthermore, in order to get full coverage, code authors will often have to re-organize their code so that it is more modular, so that each component can be tested separately, which reduces interdependencies between modules and layers, and makes for code that is easier to reason about and audit.

*There are 1 instance(s) of this issue:*

```solidity
/// @audit Global finding.
```


*GitHub* : [0](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1)
### [N&#x2011;62]<a name="N-62"></a> Large or complicated code bases should implement invariant tests
This includes: large code bases, or code with lots of inline-assembly, complicated math, or complicated interactions between multiple contracts.
Invariant fuzzers such as Echidna require the test writer to come up with invariants which should not be violated under any circumstances, and the fuzzer tests various inputs and function calls to ensure that the invariants always hold.
Even code with 100% code coverage can still have bugs due to the order of the operations a user performs, and invariant fuzzers may help significantly.

*There are 1 instance(s) of this issue:*

```solidity
/// @audit Global finding.
```


*GitHub* : [0](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1)
### [N&#x2011;63]<a name="N-63"></a> Top-level declarations should be separated by at least two lines
-

*There are 12 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}2: pragma solidity 0.8.19;
3: 
4: import {ERC1155} from "@openzeppelin/contracts/token/ERC1155/ERC1155.sol";

8: import {Turnstile} from "../interface/Turnstile.sol";
9: 
10: contract Market is ERC1155, Ownable2Step {

270:     }
271: 
272:     function _getRewardsSinceLastClaim(uint256 _id) internal view returns (uint256 amount) {
```


*GitHub* : [270-272](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L270-L272),[8-10](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L8-L10),[2-4](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L2-L4)

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}2: pragma solidity 0.8.19;
3: 
4: import {IBondingCurve} from "../../interface/IBondingCurve.sol";

4: import {IBondingCurve} from "../../interface/IBondingCurve.sol";
5: 
6: contract LinearBondingCurve is IBondingCurve {

12:     }
13: 
14:     function getPriceAndFee(uint256 shareCount, uint256 amount)

25:     }
26: 
27:     function getFee(uint256 shareCount) public pure override returns (uint256) {
```


*GitHub* : [2-4](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L2-L4),[4-6](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L4-L6),[12-14](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L12-L14),[25-27](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L25-L27)

```solidity
File: asD/src/asD.sol

}2: pragma solidity >=0.8.0;
3: 
4: import {Turnstile} from "../interface/Turnstile.sol";

9: import {SafeERC20} from "@openzeppelin/contracts/token/ERC20/utils/SafeERC20.sol";
10: 
11: contract asD is ERC20, Ownable2Step {
```


*GitHub* : [2-4](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L2-L4),[9-11](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L9-L11)

```solidity
File: asD/src/asDFactory.sol

}2: pragma solidity >=0.8.0;
3: 
4: import {Turnstile} from "../interface/Turnstile.sol";

6: import {asD} from "./asD.sol";
7: 
8: contract asDFactory is Ownable2Step {

31:     }
32: 
33:     function create(string memory _name, string memory _symbol) external returns (address) {
```


*GitHub* : [2-4](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L2-L4),[31-33](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L31-L33),[6-8](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L6-L8)
### [N&#x2011;64]<a name="N-64"></a> Consider adding formal verification proofs
Formal verification is the act of proving or disproving the correctness of intended algorithms underlying a system with respect to a certain formal specification/property/invariant, using formal methods of mathematics.

Some tools that are currently available to perform these tests on smart contracts are [SMTChecker](https://docs.soliditylang.org/en/latest/smtchecker.html) and [Certora Prover](https://www.certora.com/).

*There are 4 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}```


*GitHub* : [0](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol)

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}```


*GitHub* : [0](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol)

```solidity
File: asD/src/asD.sol

}```


*GitHub* : [0](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol)

```solidity
File: asD/src/asDFactory.sol

}```


*GitHub* : [0](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol)
### [N&#x2011;65]<a name="N-65"></a> Error messages should be descriptive, not cryptic
Consider make these error messages more descriptive.

*There are 6 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}81:         require(
82:             !shareCreationRestricted || whitelistedShareCreators[msg.sender] || msg.sender == owner(),
83:             "Not allowed"
84:         );

105:         require(whitelistedBondingCurves[_bondingCurve] != _newState, "State already set");

301:         require(shareCreationRestricted != _isRestricted, "State already set");

310:         require(whitelistedShareCreators[_address] != _isWhitelisted, "State already set");
```


*GitHub* : [301](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L301),[105](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L105),[81-84](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L81-L84),[310](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L310)

```solidity
File: asD/src/asD.sol

}64:         require(returnCode == 0, "Error when redeeming"); // 0 on success: https://docs.compound.finance/v2/ctokens/#redeem-underlying

86:         require(returnCode == 0, "Error when redeeming"); // 0 on success: https://docs.compound.finance/v2/ctokens/#redeem
```


*GitHub* : [86](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L86),[64](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L64)### Disputed Risk Issues


### [D&#x2011;01]<a name="D-01"></a> Using `private` rather than `public` for constants, saves gas
If needed, the values can be read from the verified contract source code, or if there are multiple values there can be a single getter function that [returns a tuple](https://github.com/code-423n4/2022-08-frax/blob/90f55a9ce4e25bceed3a74290b854341d8de6afa/src/contracts/FraxlendPair.sol#L156-L178) of the values of all currently-public constants. Saves **3406-3606 gas** in deployment gas due to the compiler not having to create non-payable getter functions for deployment calldata, not having to store the bytes of the value outside of where it's used, and not adding another entry to the method ID table

*There are 4 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}20:     IERC20 public immutable token;
```


*GitHub* : [20](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L20)

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}8:     uint256 public immutable priceIncrease;
```


*GitHub* : [8](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L8)

```solidity
File: asD/src/asD.sol

}15:     address public immutable cNote; // Reference to the cNOTE token
```


*GitHub* : [15](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L15)

```solidity
File: asD/src/asDFactory.sol

}12:     address public immutable cNote;
```


*GitHub* : [12](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L12)
### [D&#x2011;02]<a name="D-02"></a> Event names should use CamelCase
The instances below are already CamelCase (events are supposed to use CamelCase, not lowerCamelCase).

*There are 12 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}69:     event BondingCurveStateChange(address indexed curve, bool isWhitelisted);

70:     event ShareCreated(uint256 indexed id, string name, address indexed bondingCurve, address indexed creator);

71:     event SharesBought(uint256 indexed id, address indexed buyer, uint256 amount, uint256 price, uint256 fee);

72:     event SharesSold(uint256 indexed id, address indexed seller, uint256 amount, uint256 price, uint256 fee);

73:     event NFTsCreated(uint256 indexed id, address indexed creator, uint256 amount, uint256 fee);

74:     event NFTsBurned(uint256 indexed id, address indexed burner, uint256 amount, uint256 fee);

75:     event PlatformFeeClaimed(address indexed claimer, uint256 amount);

76:     event CreatorFeeClaimed(address indexed claimer, uint256 indexed id, uint256 amount);

77:     event HolderFeeClaimed(address indexed claimer, uint256 indexed id, uint256 amount);

78:     event ShareCreationRestricted(bool isRestricted);
```


*GitHub* : [72](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L72),[73](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L73),[74](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L74),[75](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L75),[76](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L76),[77](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L77),[78](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L78),[69](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L69),[70](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L70),[71](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L71)

```solidity
File: asD/src/asD.sol

}20:     event CarryWithdrawal(uint256 amount);
```


*GitHub* : [20](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L20)

```solidity
File: asD/src/asDFactory.sol

}20:     event CreatedToken(address token, string symbol, string name, address creator);
```


*GitHub* : [20](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L20)
### [D&#x2011;03]<a name="D-03"></a> Avoid double casting
The rule is valid, but the following findings are invalid.

*There are 1 instance(s) of this issue:*

```solidity
File: asD/src/asD.sol

}87:         IERC20 note = IERC20(CErc20Interface(cNote).underlying());
```


*GitHub* : [87](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L87)
### [D&#x2011;04]<a name="D-04"></a> Event is missing `indexed` fields
The rule is valid, but the following findings are invalid.

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}70:     event ShareCreated(uint256 indexed id, string name, address indexed bondingCurve, address indexed creator);
```


*GitHub* : [70](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L70)
### [D&#x2011;05]<a name="D-05"></a> `internal` functions only called once can be inlined to save gas
The rule is valid, but the following findings are invalid.

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}42:     function log2(uint256 x) internal pure returns (uint256 r) {
```


*GitHub* : [42](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L42)
### [D&#x2011;06]<a name="D-06"></a> Variables should be named in mixedCase style
As the [Solidity Style Guide](https://docs.soliditylang.org/en/latest/style-guide.html#naming-styles) suggests: arguments, local variables and mutable state variables should be named in mixedCase style.

*There are 1 instance(s) of this issue:*

```solidity
File: asD/src/asDFactory.sol

}/// @audit isAsD
15:     mapping(address => bool) public isAsD;
```


*GitHub* : [15](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L15)
### [D&#x2011;07]<a name="D-07"></a> safeMint should be used in place of mint
The following are not `ERC721.mint()` calls.

*There are 3 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}214:         _mint(msg.sender, _id, _amount, "");
```


*GitHub* : [214](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L214)

```solidity
File: asD/src/asD.sol

}52:         uint256 returnCode = cNoteToken.mint(_amount);

55:         _mint(msg.sender, _amount);
```


*GitHub* : [52](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L52),[55](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L55)
### [D&#x2011;08]<a name="D-08"></a> `x += y` is more expensive than `x = x + y` for state variables
It is not applicable to complex state variables.

*There are 12 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}161:         shareData[_id].tokenCount += _amount;

162:         shareData[_id].tokensInCirculation += _amount;

163:         tokensByAddress[_id][msg.sender] += _amount;

182:         shareData[_id].tokenCount -= _amount;

183:         shareData[_id].tokensInCirculation -= _amount;

184:         tokensByAddress[_id][msg.sender] -= _amount; // Would underflow if user did not have enough tokens

211:         tokensByAddress[_id][msg.sender] -= _amount;

212:         shareData[_id].tokensInCirculation -= _amount;

234:         tokensByAddress[_id][msg.sender] += _amount;

235:         shareData[_id].tokensInCirculation += _amount;

288:         shareData[_id].shareCreatorPool += shareCreatorFee;

290:             shareData[_id].shareHolderRewardsPerTokenScaled += (shareHolderFee * 1e18) / _tokenCount;
```


*GitHub* : [235](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L235),[161](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L161),[162](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L162),[163](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L163),[182](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L182),[183](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L183),[184](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L184),[211](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L211),[212](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L212),[234](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L234),[290](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L290),[288](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L288)
### [D&#x2011;09]<a name="D-09"></a> Revert on transfer to the zero address
The rule is valid, but the following findings are invalid.

*There are 13 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}153:         SafeERC20.safeTransferFrom(token, msg.sender, address(this), price + fee);

166:             SafeERC20.safeTransfer(token, msg.sender, rewardsSinceLastClaim);

187:         SafeERC20.safeTransfer(token, msg.sender, rewardsSinceLastClaim + price - fee);

206:         SafeERC20.safeTransferFrom(token, msg.sender, address(this), fee);

217:             SafeERC20.safeTransfer(token, msg.sender, rewardsSinceLastClaim);

229:         SafeERC20.safeTransferFrom(token, msg.sender, address(this), fee);

238:         SafeERC20.safeTransfer(token, msg.sender, rewardsSinceLastClaim);

247:         SafeERC20.safeTransfer(token, msg.sender, amount);

257:         SafeERC20.safeTransfer(token, msg.sender, amount);

267:             SafeERC20.safeTransfer(token, msg.sender, amount);
```


*GitHub* : [187](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L187),[153](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L153),[166](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L166),[206](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L206),[217](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L217),[229](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L229),[238](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L238),[247](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L247),[257](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L257),[267](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L267)

```solidity
File: asD/src/asD.sol

}50:         SafeERC20.safeTransferFrom(note, msg.sender, address(this), _amount);

66:         SafeERC20.safeTransfer(note, msg.sender, _amount);

88:         SafeERC20.safeTransfer(note, msg.sender, _amount);
```


*GitHub* : [50](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L50),[66](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L66),[88](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L88)
### [D&#x2011;10]<a name="D-10"></a> `SafeTransferLib` does not ensure that the token contract exists
There is a subtle difference between the implementation of solady/solmate's `SafeTransferLib` and OZ's SafeERC20. OZ's SafeERC20 checks if the token is a contract or not, while [`SafeTransferLib` does not](https://github.com/transmissions11/solmate/blob/fadb2e2778adbf01c80275bfb99e5c14969d964b/src/utils/SafeTransferLib.sol#L9):

`@dev Note that none of the functions in this library check that a token has code at all! That responsibility is delegated to the caller.`

*There are 14 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}153:         SafeERC20.safeTransferFrom(token, msg.sender, address(this), price + fee);

166:             SafeERC20.safeTransfer(token, msg.sender, rewardsSinceLastClaim);

187:         SafeERC20.safeTransfer(token, msg.sender, rewardsSinceLastClaim + price - fee);

206:         SafeERC20.safeTransferFrom(token, msg.sender, address(this), fee);

217:             SafeERC20.safeTransfer(token, msg.sender, rewardsSinceLastClaim);

229:         SafeERC20.safeTransferFrom(token, msg.sender, address(this), fee);

238:         SafeERC20.safeTransfer(token, msg.sender, rewardsSinceLastClaim);

247:         SafeERC20.safeTransfer(token, msg.sender, amount);

257:         SafeERC20.safeTransfer(token, msg.sender, amount);

267:             SafeERC20.safeTransfer(token, msg.sender, amount);
```


*GitHub* : [187](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L187),[206](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L206),[217](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L217),[229](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L229),[238](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L238),[247](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L247),[267](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L267),[257](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L257),[153](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L153),[166](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L166)

```solidity
File: asD/src/asD.sol

}50:         SafeERC20.safeTransferFrom(note, msg.sender, address(this), _amount);

51:         SafeERC20.safeApprove(note, cNote, _amount);

66:         SafeERC20.safeTransfer(note, msg.sender, _amount);

88:         SafeERC20.safeTransfer(note, msg.sender, _amount);
```


*GitHub* : [66](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L66),[50](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L50),[51](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L51),[88](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L88)
### [D&#x2011;11]<a name="D-11"></a> Solidity version 0.8.20 or above may not work on other chains due to PUSH0
The rule is invalid for this project

*There are 2 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}2: pragma solidity 0.8.19;
```


*GitHub* : [2](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L2)

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}2: pragma solidity 0.8.19;
```


*GitHub* : [2](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L2)
### [D&#x2011;12]<a name="D-12"></a> SPDX identifier should be the in the first line of a solidity file
SPDX identifier should be the in the first line of a solidity file.

*There are 4 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}1: // SPDX-License-Identifier: GPL-3.0-only
```


*GitHub* : [1](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L1)

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}1: // SPDX-License-Identifier: GPL-3.0-only
```


*GitHub* : [1](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L1)

```solidity
File: asD/src/asD.sol

}1: // SPDX-License-Identifier: GPL-3.0-only
```


*GitHub* : [1](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L1)

```solidity
File: asD/src/asDFactory.sol

}1: // SPDX-License-Identifier: GPL-3.0-only
```


*GitHub* : [1](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L1)
### [D&#x2011;13]<a name="D-13"></a> Numbers downcast to `address`es may result in collisions
The rule is valid, but the following findings are invalid.

*There are 8 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}153:         SafeERC20.safeTransferFrom(token, msg.sender, address(this), price + fee);

206:         SafeERC20.safeTransferFrom(token, msg.sender, address(this), fee);

229:         SafeERC20.safeTransferFrom(token, msg.sender, address(this), fee);
```


*GitHub* : [206](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L206),[153](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L153),[229](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L229)

```solidity
File: asD/src/asD.sol

}50:         SafeERC20.safeTransferFrom(note, msg.sender, address(this), _amount);

75:         uint256 maximumWithdrawable = (CTokenInterface(cNote).balanceOf(address(this)) * exchangeRate) /
```


*GitHub* : [50](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L50),[75](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L75)

```solidity
File: asD/src/asDFactory.sol

}35:         isAsD[address(createdToken)] = true;

36:         emit CreatedToken(address(createdToken), _symbol, _name, msg.sender);

37:         return address(createdToken);
```


*GitHub* : [36](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L36),[35](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L35),[37](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L37)
### [D&#x2011;14]<a name="D-14"></a> Unused named return
The rule is valid, but the following findings are invalid.

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}/// @audit r is used in assembly
42:     function log2(uint256 x) internal pure returns (uint256 r) {
```


*GitHub* : [42](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L42)
### [D&#x2011;15]<a name="D-15"></a> Unused named return variables without optimizer waste gas
Suggestions that only apply when the optimizer is _off_ are not useful to sponsors. Why would they pay for gas optimizations if they don't have the optimizer on, and don't plan to turn it on? Only a [small minority](https://github.com/search?q=org%3Acode-423n4+%22optimizer+%3D+false%22&type=code) have the optimizer off; the majority have it set to more than [200](https://github.com/search?q=org%3Acode-423n4+optimizer_runs&type=code) runs

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}/// @audit r is used in assembly
42:     function log2(uint256 x) internal pure returns (uint256 r) {
```


*GitHub* : [42](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L42)
### [D&#x2011;16]<a name="D-16"></a> Using bitmap to store bool states can save gas
None of these are examples where bitmaps can be used

*There are 3 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}49:     mapping(address => bool) public whitelistedBondingCurves;

64:     mapping(address => bool) public whitelistedShareCreators;
```


*GitHub* : [64](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L64),[49](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L49)

```solidity
File: asD/src/asDFactory.sol

}15:     mapping(address => bool) public isAsD;
```


*GitHub* : [15](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L15)
### [D&#x2011;17]<a name="D-17"></a> Using `delete` statement can save gas
Using delete instead of assigning zero to state variables does not save any extra gas with the optimizer [on](https://gist.github.com/IllIllI000/ef8ec3a70aede7f12433fe63dc418515#with-the-optimizer-set-at-200-runs) (saves 5-8 gas with optimizer completely off), so this finding is invalid, especially since if they were interested in gas savings, they'd have the optimizer enabled.

*There are 2 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}246:         platformPool = 0;

256:         shareData[_id].shareCreatorPool = 0;
```


*GitHub* : [246](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L246),[256](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L256)
### [D&#x2011;18]<a name="D-18"></a> Use `!= 0` or `== 0` for unsigned integer comparison
Only valid prior to solidity version 0.8.13, and only for require() statements, and at least one of those is not true for the examples below.

*There are 4 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}165:         if (rewardsSinceLastClaim > 0) {

216:         if (rewardsSinceLastClaim > 0) {

266:         if (amount > 0) {

289:         if (_tokenCount > 0) {
```


*GitHub* : [289](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L289),[165](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L165),[216](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L216),[266](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L266)
### [D&#x2011;19]<a name="D-19"></a> Avoid contract existence checks by using low level calls
Prior to 0.8.10 the compiler inserted extra code, including EXTCODESIZE (100 gas), to check for contract existence for external function calls. In more recent solidity versions, the compiler will not insert these checks if the external call has a return value. Similar behavior can be achieved in earlier versions by using low-level calls, since low level calls never check for contract existence.

*There are 6 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}/// @audit Return value not used.
96:             turnstile.register(tx.origin);

/// @audit Invalid for solidity version >= 0.8.10
135:         (price, fee) = IBondingCurve(bondingCurve).getPriceAndFee(shareData[_id].tokenCount + 1, _amount);

/// @audit Invalid for solidity version >= 0.8.10
144:         (price, fee) = IBondingCurve(bondingCurve).getPriceAndFee(shareData[_id].tokenCount - _amount + 1, _amount);

/// @audit Invalid for solidity version >= 0.8.10
196:         (uint256 priceForOne, ) = IBondingCurve(bondingCurve).getPriceAndFee(shareData[_id].tokenCount, 1);
```


*GitHub* : [144](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L144),[96](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L96),[135](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L135),[196](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L196)

```solidity
File: asD/src/asD.sol

}/// @audit Return value not used.
40:             turnstile.register(_csrRecipient);
```


*GitHub* : [40](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L40)

```solidity
File: asD/src/asDFactory.sol

}/// @audit Return value not used.
29:             turnstile.register(tx.origin);
```


*GitHub* : [29](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L29)
### [D&#x2011;20]<a name="D-20"></a> Use Ownable2Step instead of Ownable
[`Ownable2Step`](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/3d7a93876a2e5e1d7fe29b5a0e96e222afdc4cfa/contracts/access/Ownable2Step.sol#L31-L56) and [`Ownable2StepUpgradeable`](https://github.com/OpenZeppelin/openzeppelin-contracts-upgradeable/blob/25aabd286e002a1526c345c8db259d57bdf0ad28/contracts/access/Ownable2StepUpgradeable.sol#L47-L63) prevent the contract ownership from mistakenly being transferred to an address that cannot handle it (e.g. due to a typo in the address), by requiring that the recipient of the owner permissions actively accept via a contract call of its own.

*There are 3 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}10: contract Market is ERC1155, Ownable2Step {
```


*GitHub* : [10](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L10)

```solidity
File: asD/src/asD.sol

}11: contract asD is ERC20, Ownable2Step {
```


*GitHub* : [11](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L11)

```solidity
File: asD/src/asDFactory.sol

}8: contract asDFactory is Ownable2Step {
```


*GitHub* : [8](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L8)
### [D&#x2011;21]<a name="D-21"></a> Events that mark critical parameter changes should contain both the old and the new value
This should especially be done if the new value is not required to be different from the old value.

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}107:         emit BondingCurveStateChange(_bondingCurve, _newState);
```


*GitHub* : [107](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L107)
### [D&#x2011;22]<a name="D-22"></a> `safeTransfer` function does not check for contract existence
The examples below are either not token transfers, or are making high-level `transfer()`/`transferFrom()` calls (which check for contract existence), or are from a library that checks for contract existence.

*There are 4 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}91:     constructor(string memory _uri, address _paymentToken) ERC1155(_uri) Ownable() {
```


*GitHub* : [91](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L91)

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}10:     constructor(uint256 _priceIncrease) {
```


*GitHub* : [10](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L10)

```solidity
File: asD/src/asD.sol

}28:     constructor(
```


*GitHub* : [28](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L28)

```solidity
File: asD/src/asDFactory.sol

}24:     constructor(address _cNote) {
```


*GitHub* : [24](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asDFactory.sol#L24)
### [D&#x2011;23]<a name="D-23"></a> Assembly block creates dirty bits
Writing data to the free memory pointer without later updating the free memory pointer will cause there to be dirty bits at that memory location. Not updating the free memory pointer will make it [harder](https://docs.soliditylang.org/en/latest/ir-breaking-changes.html#cleanup) for the optimizer to reason about whether the memory needs to be cleaned before use, which will lead to worse optimizations. Update the free memory pointer and annotate the block (`assembly ("memory-safe") { ... }`) to avoid this issue.

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}44:         assembly {
```


*GitHub* : [44](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L44)
### [D&#x2011;24]<a name="D-24"></a> `require()` or `revert()` statements that check input arguments should be at the top of the function
The rule is valid, but the following findings are invalid.

*There are 4 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/Market.sol

}/// @audit should check before line 119
120:         require(shareIDs[_shareName] == 0, "Share already exists");
```


*GitHub* : [120](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/Market.sol#L120)

```solidity
File: asD/src/asD.sol

}/// @audit should check before line 48
54:         require(returnCode == 0, "Error when minting");

/// @audit should check before line 61
64:         require(returnCode == 0, "Error when redeeming"); // 0 on success: https://docs.compound.finance/v2/ctokens/#redeem-underlying

/// @audit should check before line 73
86:         require(returnCode == 0, "Error when redeeming"); // 0 on success: https://docs.compound.finance/v2/ctokens/#redeem
```


*GitHub* : [86](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L86),[54](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L54),[64](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L64)
### [D&#x2011;25]<a name="D-25"></a> Division by zero not prevented
The divisions below take an input parameter that has no zero-value checks, which can cause the functions reverting if zero is passed.

*There are 1 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}35:         return 1e17 / divisor;
```


*GitHub* : [35](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L35)
### [D&#x2011;26]<a name="D-26"></a> Inconsistent spacing in comments
The comments below are in the `//x` format, which differs from the commonly used idiomatic comment syntax of `//<space>x`. It is recommended to use a consistent comment syntax throughout.

*There are 4 instance(s) of this issue:*

```solidity
File: 1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol

}/// @audit It is an URL
41:     /// @notice Copied from Solady: https://github.com/Vectorized/solady/blob/main/src/utils/FixedPointMathLib.sol
```


*GitHub* : [41](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/1155tech-contracts/src/bonding_curve/LinearBondingCurve.sol#L41)

```solidity
File: asD/src/asD.sol

}/// @audit It is an URL
53:         // Mint returns 0 on success: https://docs.compound.finance/v2/ctokens/#mint

/// @audit It is an URL
64:         require(returnCode == 0, "Error when redeeming"); // 0 on success: https://docs.compound.finance/v2/ctokens/#redeem-underlying

/// @audit It is an URL
86:         require(returnCode == 0, "Error when redeeming"); // 0 on success: https://docs.compound.finance/v2/ctokens/#redeem
```


*GitHub* : [86](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L86),[53](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L53),[64](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L64)
### [D&#x2011;27]<a name="D-27"></a> Consider activating via-ir for deploying
The rule is invalid for this project

*There are 1 instance(s) of this issue:*

```solidity
/// @audit Global finding.
```


*GitHub* : [0](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1)
### [D&#x2011;28]<a name="D-28"></a> Enable IR-based code generation
The rule is invalid for this project

*There are 1 instance(s) of this issue:*

```solidity
/// @audit Global finding.
```


*GitHub* : [0](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1)
### [D&#x2011;29]<a name="D-29"></a> Large approvals may not work with some `ERC20` tokens
Some tokens such as [COMP](https://github.com/compound-finance/compound-protocol/blob/a3214f67b73310d547e00fc578e8355911c9d376/contracts/Governance/Comp.sol#L89-L91) downcast such approvals to `uint96` and use that as a raw value rather than interpreting it as an infinite approval. Eventually these approvals will reach zero, at which point the calling contract will no longer function properly.

*There are 1 instance(s) of this issue:*

```solidity
File: asD/src/asD.sol

}51:         SafeERC20.safeApprove(note, cNote, _amount);
```


*GitHub* : [51](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L51)
### [D&#x2011;30]<a name="D-30"></a> Contracts are vulnerable to rebasing accounting-related issues
The rule is invalid for this project

*There are 1 instance(s) of this issue:*

```solidity
File: asD/src/asD.sol

}72:     function withdrawCarry(uint256 _amount) external onlyOwner {
```


*GitHub* : [72](https://github.com/code-423n4/2023-11-canto/blob/516099801101950ac9e1117a70e095b06f9bf6a1/asD/src/asD.sol#L72) Thanks for reading!