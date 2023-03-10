# Wrapped ERC20 Token
wrappedToken use for all ERC20 token, example: **WETH** for **ETH**.

### deploy
- copy ERC20 address (for example deploy erc20 Mock)
- paste address as value in Wrapped contract constructor + name + symbol
- before anything: approve wrapped contract as/is spender from base erc20 token
- `deposit` : make wrapped token and locked base token
- `withdraw` : burn wrapped and return locked token to the life cycle
- other functions same an ERC20

### develop
- using `IWrapped` interface is custom/optional : if using this intrface, then inherit erc165 & inherite Wrapped contract. need to register

### libraries
in this example use @openzeppelin/contracts --> sub --> erc20

**if you like to use flat version, use** [this](https://testnet.bscscan.com/address/0x33a1ef3987181e09d3e498ba1c1d53f380b46426#code) 

#

> 07-12-2022 live stream

---

### ready/deployed
- [ERC20 Token](https://testnet.bscscan.com/address/0x22ac23beba298a839657949d1279f886b7a4df50) 
- [Wrapped Token](https://testnet.bscscan.com/address/0x33a1ef3987181e09d3e498ba1c1d53f380b46426) 

---

### contract info 

|  Contract  |         Type        |       Bases      |                  |                 |
|:----------:|:-------------------:|:----------------:|:----------------:|:---------------:|
|     â      |  **Function Name**  |  **Visibility**  |  **Mutability**  |  **Modifiers**  |
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


 Legend

|  Symbol  |  Meaning  |
|:--------:|-----------|
|    ð    | Function can modify state |
|    ðµ    | Function is payable |

  
  ### signature hash
  
|  Sighash   |   Function Signature | 
| ---- | ---- | 
| cb03a464  |  isBalanced() | 
| e5347ed9  |  returnDecimals(address) | 
| a3496274  |  returnBalances() | 
| f61ecc61  |  returnDeposited() | 
| 146cf9fb  |  returnDeposited(address) | 
| b6b55f25  |  deposit(uint256) | 
| 2e1a7d4d  |  withdraw(uint256) | 
| f3fef3a3  |  withdraw(address,uint256) | 
| 590e1ae3  |  refund() | 
| 510e01ac  |  _terminate() | 
| a0712d68  |  mint(uint256) | 
| 42966c68  |  burn(uint256) | 
| d51f0f47  |  _decimals(address) | 
