# Proof Of Exist

in this *industry* (decentralized world) we need to **proof* anything before calculate. the #proof_of_exist is near the #MerkleProof , just another strategy...

> live stream - 5Aug 2022

### how to test:
- **deploy**
- for *simulating the transaction* run **`generate`** function
- for *check exist transaction* run other *4 function's*

**enjoy it!**

---

## web3 ui

- index.html
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Blockchain Simulation Web3 UI</title>
    <link rel="stylesheet" href="./tailwind.min.css">
  </head>
  <body class="bg-gray-100">
    <div class="container mx-auto px-4 py-8">
      <h1 class="text-3xl font-bold mb-4">Blockchain Simulation Web3 UI</h1>
      <div class="mb-4">
        <p class="font-bold mb-2">Current block:</p>
        <p class="whitespace-pre-wrap bg-gray-200 rounded-lg p-2">{{ currentBlock }}</p>
      </div>
      <form class="mb-4" @submit.prevent="generateBlock">
        <label class="font-bold mb-2 block" for="data-input">Data:</label>
        <input class="border border-gray-400 rounded-lg px-2 py-1 w-full mb-2" type="text" id="data-input" v-model="data">
        <button class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded" type="submit">Generate block</button>
      </form>
      <div class="mb-4" v-if="proof">
        <p class="font-bold mb-2">Proof:</p>
        <p class="whitespace-pre-wrap bg-gray-200 rounded-lg p-2">{{ proof }}</p>
      </div>
      <form class="mb-4" @submit.prevent="checkProof">
        <label class="font-bold mb-2 block" for="proof-input">Proof:</label>
        <input class="border border-gray-400 rounded-lg px-2 py-1 w-full mb-2" type="text" id="proof-input" v-model="proofInput">
        <button class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded" type="submit">Check proof</button>
      </form>
      <div v-if="proofResult !== null">
        <p class="font-bold mb-2">Check result:</p>
        <p v-if="proofResult" class="text-green-600 font-bold">Valid proof!</p>
        <p v-else class="text-red-600 font-bold">Invalid proof!</p>
      </div>
    </div>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/ethers@5.5.4/dist/ethers.min.js"></script>
    <script src="./app.js"></script>
  </body>
</html>
```

- app.js
```js
// connect to Ethereum network using ethers.js and Metamask
const provider = new ethers.providers.Web3Provider(window.ethereum);
const signer = provider.getSigner();
const contractAddress = "CONTRACT_ADDRESS";
const abi = CONTRACT_ABI;
const contract = new ethers.Contract(contractAddress, abi, signer);

// Vue.js app
const app = new Vue({
  el: "#app",
  data: {
    data: "",
    currentBlock: "",
    proof: "",
    proofInput: "",
    proofResult: null,
  },
  async mounted() {
    // get current block
    const currentBlock = await contract.generate();
    this.currentBlock = currentBlock;
  },
  methods: {
    async generateBlock() {
      // generate new block
      const newBlock = await contract.generate(this.data);
      this.currentBlock = newBlock;
      this.data = "";
    },
    async checkProof() {
      // check proof
      const proof = this.proofInput;
      const isValid = await contract.checkProof(proof);
      this.proofResult = isValid;
    },
  },
});
```
