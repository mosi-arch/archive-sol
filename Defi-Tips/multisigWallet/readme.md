# Multisig Wallet

- in this version i try to : 
- - working by mapping like a database.
- - save gas 

### there is a bug: 
- in the `constructor` would to check : **owners >= signers(validators)**
- for fix in backend just check
- or in frontend check those values

> live stream at 06-20-2022

---

in test on remix, i use this accounts as owners
```
["0x5B38Da6a701c568545dCfcB03FcB875f56beddC4",
"0xAb8483F64d9C6d1EcF9b849Ae677dD3315835cb2",
"0x4B20993Bc481177ec7E8f571ceCaE8A9e22C02db"]
```
and use this account is/as recipient 
`0xdD870fA1b7C4700F2BD7f44238821C26f7392148`

---

### contract info

|  Contract  |         Type        |       Bases      |                  |                 |
|:----------:|:-------------------:|:----------------:|:----------------:|:---------------:|
|     â      |  **Function Name**  |  **Visibility**  |  **Mutability**  |  **Modifiers**  |
||||||
| **MultiSigWallet** | Implementation |  |||
| â | _onlyOwner | Private ð |   | |
| â | _onlySigner | Private ð |   | |
| â | <Constructor> | Public âï¸ | ð  |NOâï¸ |
| â | <Fallback> | External âï¸ |  ðµ |NOâï¸ |
| â | <Receive Ether> | External âï¸ |  ðµ |NOâï¸ |
| â | deposit | Public âï¸ |  ðµ |NOâï¸ |
| â | withdraw | Private ð | ð  | onlySigner |
| â | submit | Public âï¸ | ð  | onlySigner |
| â | confirm | Public âï¸ | ð  | onlySigner |
| â | revoke | Public âï¸ | ð  | onlySigner |
| â | balance | Public âï¸ |   |NOâï¸ |
| â | investor | Public âï¸ |   |NOâï¸ |
| â | investor | Public âï¸ |   |NOâï¸ |
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
||||||
| **Recurit** | Implementation | Ownable |||
| â | finish | Public âï¸ | ð  |NOâï¸ |
| â | depositsOf | Public âï¸ |   |NOâï¸ |
| â | deposit | External âï¸ |  ðµ | onlyOwner |
| â | withdraw | External âï¸ | ð  | onlyOwner |
| â | _deposit | Internal ð | ð  | onlyOwner |
| â | _withdraw | Internal ð | ð  | onlyOwner |
||||||
| **Wrapped** | Implementation | ERC20 |||
| â | <Constructor> | Public âï¸ | ð  | ERC20 |
| â | isBalanced | Internal ð |   | |
| â | returnDecimals | Public âï¸ |   |NOâï¸ |
| â | returnBalances | Public âï¸ |   |NOâï¸ |
| â | returnDeposited | Public âï¸ |   |NOâï¸ |
| â | returnDeposited | Public âï¸ |   |NOâï¸ |
| â | deposit | External âï¸ | ð  |NOâï¸ |
| â | withdraw | External âï¸ | ð  |NOâï¸ |
| â | withdraw | External âï¸ | ð  |NOâï¸ |
| â | refund | External âï¸ | ð  |NOâï¸ |
| â | _terminate | Internal ð | ð  | |
| â | mint | Internal ð | ð  | |
| â | burn | Internal ð | ð  | |
| â | _decimals | Private ð |   | |


 Legend

|  Symbol  |  Meaning  |
|:--------:|-----------|
|    ð    | Function can modify state |
|    ðµ    | Function is payable |

### signature hash

| Sighash   |   Function Signature | 
| ---- | ---- | 
| 71dfb281  |  _onlyOwner() | 
| 4cc81585  |  _onlySigner() | 
| d0e30db0  |  deposit() | 
| e63697c8  |  withdraw(uint256,address,uint256) | 
| 203dd666  |  submit(address,uint256) | 
| ba0179b5  |  confirm(uint256) | 
| 20c5429b  |  revoke(uint256) | 
| b69ef8a8  |  balance() | 
| 1e0018d6  |  investor() | 
| 1b1cd4ff  |  investor(address) | 
