## Stake NFT for Reward


- remember to approve contract to use token
- make `erc20` & `erc721` for test

### learn about `stake logic` [here](https://github.com/mosi-sol/live-contracts-s2/tree/main/05-simple-staking) 

##

expermential code & idea. this kind of dapp can be the next hype or wave. (3rd generation of dapp`s)


##

- decress reward by decressing value from `100` in `line 8`


```
stake source for erc20 tokens idea & credit : https://www.smartcontract.engineer/
git: t4sk
```

<p align="right">
17Feb 2022 - live video ( learn solidity in farsi for free )
  </p>

---

### contract info

|  Contract  |         Type        |       Bases      |                  |                 |
|:----------:|:-------------------:|:----------------:|:----------------:|:---------------:|
|     â      |  **Function Name**  |  **Visibility**  |  **Mutability**  |  **Modifiers**  |
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


 Legend

|  Symbol  |  Meaning  |
|:--------:|-----------|
|    ð    | Function can modify state |
|    ðµ    | Function is payable |

### signature hash

| Sighash   |   Function Signature | 
| ---- | ---- | 
| cd3daf9d  |  rewardPerToken() | 
| 008cc262  |  earned(address) | 
| a694fc3a  |  stake(uint256) | 
| 2e1a7d4d  |  withdraw(uint256) | 
| 3d18b912  |  getReward() | 
| 18160ddd  |  totalSupply() | 
| 70a08231  |  balanceOf(address) | 
| a9059cbb  |  transfer(address,uint256) | 
| dd62ed3e  |  allowance(address,address) | 
| 095ea7b3  |  approve(address,uint256) | 
| 23b872dd  |  transferFrom(address,address,uint256) | 
| 6352211e  |  ownerOf(uint256) | 
| b88d4fde  |  safeTransferFrom(address,address,uint256,bytes) | 
| 42842e0e  |  safeTransferFrom(address,address,uint256) | 
| a22cb465  |  setApprovalForAll(address,bool) | 
| 081812fc  |  getApproved(uint256) | 
| e985e9c5  |  isApprovedForAll(address,address) | 
| 01ffc9a7  |  supportsInterface(bytes4) | 
| 150b7a02  |  onERC721Received(address,address,uint256,bytes) | 
| 06fdde03  |  name() | 
| 95d89b41  |  symbol() | 
| c87b56dd  |  tokenURI(uint256) | 
| 4f6ccce7  |  tokenByIndex(uint256) | 
| 2f745c59  |  tokenOfOwnerByIndex(address,uint256) | 
