## Escrow

- Exacutables:
- - deposit
- - finish
- - withdraw


- Readonly:
- - depositsOf

### how to:

`deploy` -> `deployer deposit` -> `crew finish job` -> `deployer sending money`

- **deploy** contract by recuriter/customer
- run **deposit** by sending a ***value & address*** of services(like a programmer)
- after finishing the job by services(programmer) runing **finish** function by him/her
- customer can to run **withdraw** function for releasing & send value

### todo:
in next version
- ``save value amount`` in a variable, delete/0 that after withdraw
- ``getter function`` for escrowID

### security
- change `internal` functions to `private`

---
<p align="right">
  <a href="https://github.com/mosi-sol" target="blank">
  <img src="https://img.shields.io/badge/Escrow-Contract-blue?style=flat" alt="cafe_pafe" /></a>  
</p>

---

### contract info

|  Contract  |         Type        |       Bases      |                  |                 |
|:----------:|:-------------------:|:----------------:|:----------------:|:---------------:|
|     â      |  **Function Name**  |  **Visibility**  |  **Mutability**  |  **Modifiers**  |
||||||
| **Recurit** | Implementation | Ownable |||
| â | finish | Public âï¸ | ð  |NOâï¸ |
| â | depositsOf | Public âï¸ |   |NOâï¸ |
| â | deposit | External âï¸ |  ðµ | onlyOwner |
| â | withdraw | External âï¸ | ð  | onlyOwner |
| â | _deposit | Internal ð | ð  | onlyOwner |
| â | _withdraw | Internal ð | ð  | onlyOwner |
||||||
| **Cipher** | Implementation |  |||
| â | compare | Internal ð |   | |
| â | morse_to_char | Internal ð |   | |
| â | char_to_morse | Internal ð |   | |
| â | hash | Internal ð |   | |
| â | dehash | Internal ð |   | |
||||||
| **Test** | Implementation | Cipher |||
| â | receiveMsg | Public âï¸ |   |NOâï¸ |
| â | sendMsg | Public âï¸ |   |NOâï¸ |
||||||
| **TestWord** | Implementation | Cipher |||
| â | concat | Internal ð |   | |
| â | morse | Public âï¸ |   |NOâï¸ |
||||||
| **Cipher** | Implementation |  |||
| â | compare | Internal ð |   | |
| â | char_to_morse_code | Internal ð |   | |
||||||
| **Test** | Implementation | Cipher |||
| â | morse | Public âï¸ |   |NOâï¸ |
||||||
| **Cipher** | Implementation |  |||
| â | <Constructor> | Public âï¸ | ð  |NOâï¸ |
| â | _design1 | Internal ð | ð  | |
| â | _design2 | Internal ð | ð  | |
| â | _T | Internal ð |   | |
| â | concat | Internal ð |   | |
| â | _generate | Internal ð |   | |
| â | _pattern_1 | Internal ð | ð  | |
| â | _pattern_2 | Internal ð | ð  | |
||||||
| **TestWord** | Implementation | Cipher |||
| â | unMerge | Public âï¸ |   |NOâï¸ |
| â | generate | Public âï¸ |   |NOâï¸ |
| â | table | Public âï¸ |   |NOâï¸ |
| â | pattern_1 | Public âï¸ | ð  |NOâï¸ |
| â | pattern_2 | Public âï¸ | ð  |NOâï¸ |
||||||
| **Cipher** | Implementation |  |||
| â | <Constructor> | Public âï¸ | ð  |NOâï¸ |
| â | _design | Private ð | ð  | |
| â | _T | Internal ð |   | |
| â | concat | Internal ð |   | |
| â | _generate | Internal ð |   | |
||||||
| **TestWord** | Implementation | Cipher |||
| â | generate | Public âï¸ |   |NOâï¸ |
| â | table | Public âï¸ |   |NOâï¸ |
||||||
| **Cipher** | Implementation |  |||
| â | compare | Internal ð |   | |
| â | _T | Internal ð |   | |
| â | T | Public âï¸ |   |NOâï¸ |
| â | isValid | Public âï¸ |   |NOâï¸ |
||||||
| **NoFeeSwap2Pairs** | Implementation |  |||
| â | <Constructor> | Public âï¸ | ð  |NOâï¸ |
| â | _lock | Private ð | ð  | |
| â | _release | Private ð | ð  | |
| â | _hold | Private ð | ð  | |
| â | createValuetion | External âï¸ | ð  |NOâï¸ |
| â | clearValuetion | External âï¸ | ð  |NOâï¸ |
| â | swap | External âï¸ | ð  | isValidToken |
| â | _min | Private ð |   | |
| â | _sqrt | Private ð |   | |
| â | sqrt_ | Private ð |   | |
| â | _this | Internal ð |   | |
| â | _msgSender | Internal ð |   | |
| â | _msgData | Internal ð |   | |
| â | _msgValue | Internal ð |   | |
||||||
| **IERC20** | Interface |  |||
| â | totalSupply | External âï¸ |   |NOâï¸ |
| â | balanceOf | External âï¸ |   |NOâï¸ |
| â | transfer | External âï¸ | ð  |NOâï¸ |
| â | allowance | External âï¸ |   |NOâï¸ |
| â | approve | External âï¸ | ð  |NOâï¸ |
| â | transferFrom | External âï¸ | ð  |NOâï¸ |
||||||
| **CrowdfundingFactory** | Implementation |  |||
| â | create | Public âï¸ | ð  |NOâï¸ |
| â | conterbute | Public âï¸ |  ðµ |NOâï¸ |
| â | refund | Public âï¸ | ð  |NOâï¸ |
| â | finalize | Public âï¸ | ð  |NOâï¸ |
| â | balanceOfCampagin | Public âï¸ |   |NOâï¸ |
| â | balance | Public âï¸ |   |NOâï¸ |
| â | version | Public âï¸ |   |NOâï¸ |
||||||
| **Crowdfunding** | Implementation |  |||
| â | _onlyAdmin | Private ð |   | |
| â | _onlyFundRaiser | Private ð |   | |
| â | _isNotEnded | Private ð |   | |
| â | _areValidToPay | Private ð |   | |
| â | <Constructor> | Public âï¸ | ð  |NOâï¸ |
| â | <Receive Ether> | External âï¸ |  ðµ |NOâï¸ |
| â | <Fallback> | External âï¸ |  ðµ |NOâï¸ |
| â | create | Public âï¸ | ð  | onlyAdmin |
| â | conterbute | Public âï¸ |  ðµ | isNotEnded |
| â | refund | Public âï¸ | ð  | onlyFundRaiser isNotEnded noReentrant |
| â | revoke | Public âï¸ | ð  | onlyAdmin |
| â | finalize | Public âï¸ | ð  | onlyAdmin |
| â | _isContract | Internal ð |   | |
| â | balance | Public âï¸ |   |NOâï¸ |
| â | balanceOf | Public âï¸ |   |NOâï¸ |
| â | balanceOfCampagin | Public âï¸ |   |NOâï¸ |
| â | changeNeedTimer | Public âï¸ |   | onlyAdmin |
| â | theVersion | Public âï¸ |   |NOâï¸ |
| â | changeVersion | Public âï¸ | ð  | onlyAdmin |
||||||
| **IERC20** | Interface |  |||
| â | totalSupply | External âï¸ |   |NOâï¸ |
| â | balanceOf | External âï¸ |   |NOâï¸ |
| â | allowance | External âï¸ |   |NOâï¸ |
| â | transfer | External âï¸ | ð  |NOâï¸ |
| â | approve | External âï¸ | ð  |NOâï¸ |
| â | transferFrom | External âï¸ | ð  |NOâï¸ |


 Legend

|  Symbol  |  Meaning  |
|:--------:|-----------|
|    ð    | Function can modify state |
|    ðµ    | Function is payable |

### signature hash

| Sighash   |   Function Signature | 
| ---- | ---- | 
| d353a1cb  |  finish(uint256) | 
| e3a9db1a  |  depositsOf(address) | 
| f340fa01  |  deposit(address) | 
| f3fef3a3  |  withdraw(address,uint256) | 
| 5415aaf2  |  _deposit(address) | 
| b790a77b  |  _withdraw(address,uint256) | 
