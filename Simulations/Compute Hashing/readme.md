# Compute Hashing
a code like a game to learn how to hashing, what is local & state variables.

`makeABlock` -> put a possitive number and check the result

---

## Web3 - UI

- index.html
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>MakeABlock Web3 UI</title>
  </head>
  <body>
    <h1>MakeABlock Web3 UI</h1>
    <p>Current value of i: <span id="i-value"></span></p>
    <form id="make-block-form">
      <label for="j-input">j:</label>
      <input type="number" id="j-input" name="j" required>
      <button type="submit">Make a block</button>
    </form>
    <p>Block hash: <span id="block-hash"></span></p>
    <script src="https://cdn.jsdelivr.net/npm/web3@1.3.5/dist/web3.min.js"></script>
    <script src="./app.js"></script>
  </body>
</html>
```

- app.js
```js
// connect to Ethereum network using web3.js and Metamask
const web3 = new Web3(window.ethereum);
await window.ethereum.enable();

// load contract using the ABI and contract address
const contractAddress = "CONTRACT_ADDRESS";
const abi = CONTRACT_ABI;
const contract = new web3.eth.Contract(abi, contractAddress);

// display current value of i
const i = await contract.methods.i().call();
document.getElementById("i-value").textContent = i;

// handle form submit to call makeABlock function
document.getElementById("make-block-form").addEventListener("submit", async (event) => {
  event.preventDefault();
  const j = event.target.elements.j.value;
  const tx = await contract.methods.makeABlock(j).send({ from: ethereum.selectedAddress });
  const blockHash = tx.events.BlockCreated.returnValues.blockHash;
  document.getElementById("block-hash").textContent = blockHash;
});
```
