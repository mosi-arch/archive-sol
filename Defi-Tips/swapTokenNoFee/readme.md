# SWAP *ERC20*
- deploy `erc20mock` contract , 2 times for `token a` & `token b`
- deploy `swap` contract , put that 2 address as value's
- don't forget to `approve` the *swap address* on that *2 mock* as *spender*
- run `createValuetion` function as liquidity pool
- with your test account or other account run `swap` function
##
- for clear liquidity run `clearValuetion` function
##
- for using another token for pair's, deploy `SWAP` contract again with *new pairs* OR
- - use factory pattern - [example](https://github.com/mosi-sol/live-contracts/tree/main/episode-3) 
- - use proxy pattern - [example](https://github.com/mosi-sol/live-contracts/tree/main/episode-23) 
- - use create2 pattern - [example](https://github.com/mosi-sol/live-contract-s3/tree/main/03-%20Create2)  
##

> BootCamp (solidity rush) - 8 hour solidity from scratch - 
BootCamp weeks ago, language farsi/persian

---

### contract info

|  Contract  |         Type        |       Bases      |                  |                 |
|:----------:|:-------------------:|:----------------:|:----------------:|:---------------:|
|     â      |  **Function Name**  |  **Visibility**  |  **Mutability**  |  **Modifiers**  |
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
| 1f73668d  |  _lock(address,uint256) |
| 0495ff94  |  _release(address,uint256) |
| ea366720  |  _hold(uint256,uint256) |
| 6f577473  |  createValuetion(uint256,uint256) |
| 94f02fc4  |  clearValuetion(uint256) |
| d004f0f7  |  swap(address,uint256) |
| ac023b75  |  _min(uint256,uint256) |
| 6a263f02  |  _sqrt(uint256) |
| 5378ae36  |  sqrt_(uint256) |
| 2b5ab84a  |  _this() |
| 119df25f  |  _msgSender() |
| 8b49d47e  |  _msgData() |
| 45ec9354  |  _msgValue() |
