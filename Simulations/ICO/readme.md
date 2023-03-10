# ICO - STO - IDO - IPO

> tester: 0xc58522826208D07A4fDAC68FEa01bE618b25685A

- mock erc20 (**PICO**) : [block explorer](https://testnet.bscscan.com/address/0x0dc313c7659fd02e1c7d247faa1075ec50f163c8#code)
- mock ico token (**TICO**) : [block explorer](https://testnet.bscscan.com/address/0xe9205ecb3c32bad2335e0e2c1a8014c9ba9ad095#code)
- **ICO** : [block explorer](https://testnet.bscscan.com/address/0xdc4227f7be667a65bd5f72b4332de1784d4b5334#code)

### how to deploy:
- choose an erc20 or deploy `PICO`
- deploy `ico`, set purchase token address -> pico
- deploy `TICO`, set address `ico`
- into `ico` set function `targetIco(tico)`
- into `ico` run function `release`

*dont forget to approve `ico` address from purchased `pico`*

*you can change amount of `tico` in `constructor` for ico*

#

**fix:**
- add `wd();` in line 86 of `ico.sol`

---

28 jul- 2022

---

### contract info 

|  Contract  |         Type        |       Bases      |                  |                 |
|:----------:|:-------------------:|:----------------:|:----------------:|:---------------:|
|     â      |  **Function Name**  |  **Visibility**  |  **Mutability**  |  **Modifiers**  |
||||||
| **ICO** | Implementation | Ownable |||
| â | <Constructor> | Public âï¸ | ð  |NOâï¸ |
| â | <Receive Ether> | External âï¸ |  ðµ |NOâï¸ |
| â | release | Public âï¸ | ð  | onlyOwner |
| â | setValue | Public âï¸ | ð  | onlyOwner |
| â | claim | Public âï¸ |  ðµ |NOâï¸ |
| â | targetIco | Public âï¸ | ð  | onlyOwner |
| â | viewHolders | Public âï¸ |   |NOâï¸ |
| â | wd | Private ð | ð  | |
||||||
| **AuctionNFT** | Implementation | Ownable, ReentrancyGuard |||
| â | <Constructor> | Public âï¸ | ð  |NOâï¸ |
| â | startAuction | External âï¸ | ð  | onlyOwner |
| â | bid | External âï¸ |  ðµ |NOâï¸ |
| â | end | External âï¸ | ð  | onlyOwner |
| â | _startAuction | Internal ð | ð  | |
| â | _bid | Internal ð | ð  | |
| â | _end | Internal ð | ð  | |
| â | withdraw | External âï¸ | ð  | nonReentrant |
| â | onERC721Received | Public âï¸ | ð  |NOâï¸ |
||||||
| **StakingRewards** | Implementation |  |||
| â | <Constructor> | Public âï¸ | ð  |NOâï¸ |
| â | rewardPerToken | Public âï¸ |   |NOâï¸ |
| â | earned | Public âï¸ |   |NOâï¸ |
| â | stake | External âï¸ | ð  | updateReward |
| â | withdraw | External âï¸ | ð  | updateReward |
| â | getReward | External âï¸ | ð  | updateReward |
||||||
| **IERC20** | Interface |  |||
| â | totalSupply | External âï¸ |   |NOâï¸ |
| â | balanceOf | External âï¸ |   |NOâï¸ |
| â | transfer | External âï¸ | ð  |NOâï¸ |
| â | allowance | External âï¸ |   |NOâï¸ |
| â | approve | External âï¸ | ð  |NOâï¸ |
| â | transferFrom | External âï¸ | ð  |NOâï¸ |
||||||
| **IERC721** | Interface |  |||
| â | balanceOf | External âï¸ |   |NOâï¸ |
| â | ownerOf | External âï¸ |   |NOâï¸ |
| â | safeTransferFrom | External âï¸ |  ðµ |NOâï¸ |
| â | safeTransferFrom | External âï¸ |  ðµ |NOâï¸ |
| â | transferFrom | External âï¸ |  ðµ |NOâï¸ |
| â | approve | External âï¸ |  ðµ |NOâï¸ |
| â | setApprovalForAll | External âï¸ | ð  |NOâï¸ |
| â | getApproved | External âï¸ |   |NOâï¸ |
| â | isApprovedForAll | External âï¸ |   |NOâï¸ |
||||||
| **IERC165** | Interface |  |||
| â | supportsInterface | External âï¸ |   |NOâï¸ |
||||||
| **IERC721TokenReceiver** | Interface |  |||
| â | onERC721Received | External âï¸ | ð  |NOâï¸ |
||||||
| **IERC721Metadata** | Interface |  |||
| â | name | External âï¸ |   |NOâï¸ |
| â | symbol | External âï¸ |   |NOâï¸ |
| â | tokenURI | External âï¸ |   |NOâï¸ |
||||||
| **IERC721Enumerable** | Interface |  |||
| â | totalSupply | External âï¸ |   |NOâï¸ |
| â | tokenByIndex | External âï¸ |   |NOâï¸ |
| â | tokenOfOwnerByIndex | External âï¸ |   |NOâï¸ |


 Legend

|  Symbol  |  Meaning  |
|:--------:|-----------|
|    ð    | Function can modify state |
|    ðµ    | Function is payable |

### signature hash 

| Sighash   |   Function Signature | 
| ---- |  ---- | 
| 55241077  |  setValue(uint256) | 
| 86d1a69f  |  release() | 
| 379607f5  |  claim(uint256) | 
| f8c99ffa  |  setValue(....,admin,amount) | 
| c7ba2f0a  |  targetIco(address) | 
| 4afe9f1d  |  viewHolders() | 
| 8edec689  |  wd() | 
