```typescript
import Web3 from 'web3';
import { Contract } from 'web3-eth-contract';

const w3 = new Web3(Web3.givenProvider || "https://cloudflare-eth.com");

const daiTokenAddr = "0x6B175474E89094C44Da98b954EedeAC495271d0F";    // DAI
const wethTokenAddr = "0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2";   // Wrapped ether (WETH)

const accAddress = "0xA478c2975Ab1Ea89e8196811F51A7B7Ade33eB11";      // Uniswap V2: DAI 2

// This is a simplified Contract Application Binary Interface (ABI) of an ERC-20 Token Contract.
// It will expose only the methods: balanceOf(address), decimals(), symbol() and totalSupply()

const simplifiedABI = [
    {
        'inputs': [{'internalType': 'address', 'name': 'account', 'type': 'address'}],
        'name': 'balanceOf',
        'outputs': [{'internalType': 'uint256', 'name': '', 'type': 'uint256'}],
        'stateMutability': 'view', 'type': 'function', 'constant': true
    },
    {
        'inputs': [],
        'name': 'decimals',
        'outputs': [{'internalType': 'uint8', 'name': '', 'type': 'uint8'}],
        'stateMutability': 'view', 'type': 'function', 'constant': true
    },
    {
        'inputs': [],
        'name': 'symbol',
        'outputs': [{'internalType': 'string', 'name': '', 'type': 'string'}],
        'stateMutability': 'view', 'type': 'function', 'constant': true
    },
    {
        'inputs': [],
        'name': 'totalSupply',
        'outputs': [{'internalType': 'uint256', 'name': '', 'type': 'uint256'}],
        'stateMutability': 'view', 'type': 'function', 'constant': true
    }
];

const daiContract = new Contract(simplifiedABI,
    w3.utils.toChecksumAddress(daiTokenAddr));

let symbol = daiContract.methods.symbol().call()
let decimals = daiContract.methods.decimals().call()
let totalSupply = daiContract.methods.totalSupply().call() / 10**decimals
let addrBalance = daiContract.methods.balanceOf(accAddress).call() / 10**decimals

// DAI
console.log(`===== ${symbol} =====`)
console.log(`Total Supply: ${totalSupply}`)
console.log(`Addr Balance: ${addrBalance}`)

const wethContract =  new Contract(simplifiedABI,
    w3.utils.toChecksumAddress(wethTokenAddr))

symbol = wethContract.methods.symbol().call()
decimals = wethContract.methods.decimals().call()
totalSupply = wethContract.methods.totalSupply().call() / 10**decimals
addrBalance = wethContract.methods.balanceOf(accAddress).call() / 10**decimals

// WETH
console.log(`===== ${symbol} =====`)
console.log(`Total Supply: ${totalSupply}`)
console.log(`Addr Balance: ${addrBalance}`)
```
