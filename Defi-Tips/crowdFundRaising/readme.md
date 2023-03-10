# Crowd Fundraising
- how to start a fund raising campagin
- how to work
- included make by factory pattern

> live stream at 06-22-2022

---

### how to use by factory
- remove or comment line 106 [here](https://github.com/mosi-sol/live-contracts-s2/blob/ef5c79a458d6c452eb535af2dad71a4221d7203b/21-Crowd%20Fund%20Raising%20part%202/CrowdFund-part2.sol#L106) 

### how to deploy & run directly
- use line 106 & compile & deploy [here](https://github.com/mosi-sol/live-contracts-s2/blob/ef5c79a458d6c452eb535af2dad71a4221d7203b/21-Crowd%20Fund%20Raising%20part%202/CrowdFund-part2.sol#L106) 

---

### contract info

|  Contract  |         Type        |       Bases      |                  |                 |
|:----------:|:-------------------:|:----------------:|:----------------:|:---------------:|
|     â      |  **Function Name**  |  **Visibility**  |  **Mutability**  |  **Modifiers**  |
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


 Legend

|  Symbol  |  Meaning  |
|:--------:|-----------|
|    ð    | Function can modify state |
|    ðµ    | Function is payable |

### signature hash

| Sighash   |   Function Signature | 
| ---- | ---- | 
| fd768f55  |  create(address,uint256,uint256,bool) | 
| 9495cd98  |  conterbute(uint256) | 
| 278ecde1  |  refund(uint256) | 
| 05261aea  |  finalize(uint256) | 
| 1bb58744  |  balanceOfCampagin(uint256) | 
| b69ef8a8  |  balance() | 
| 54fd4d50  |  version() | 
| ab2b1ca4  |  _onlyAdmin() | 
| f939c53f  |  _onlyFundRaiser() | 
| ee6c924b  |  _isNotEnded(uint256) | 
| 01af6d7e  |  _areValidToPay(uint256) | 
| 20c5429b  |  revoke(uint256) | 
| 7d48441f  |  _isContract(address) | 
| 00fdd58e  |  balanceOf(address,uint256) | 
| 5edd94a0  |  changeNeedTimer() | 
| 1d01762c  |  theVersion() | 
| 107752fe  |  changeVersion(uint256) | 
| 18160ddd  |  totalSupply() | 
| 70a08231  |  balanceOf(address) | 
| dd62ed3e  |  allowance(address,address) | 
| a9059cbb  |  transfer(address,uint256) | 
| 095ea7b3  |  approve(address,uint256) | 
| 23b872dd  |  transferFrom(address,address,uint256) | 
