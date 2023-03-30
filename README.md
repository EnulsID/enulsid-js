# ENULS Web3 Identity

Nodejs SDK

Npm: https://www.npmjs.com/package/domainchainjs

Github: https://github.com/DomainChainHQ/domainchainjs

Before installing the package you need to check and be sure to install the packages below:

```
npm install web3 
```

Install Package

```
npm install domainchainjs
```

Call 
```
const domainchainjs = require('domainchainjs');
```

Install:

Chain Supported: enuls

```
// for astar domains astr.domains
const enuls = 
{
		rpcUrl: "https://evmapi.nuls.io",
		contractAddress: "0xA1019535E6b364523949EaF45F4B17521c1cb074",
		
}

const sdk = domainchainjs.SDK('custom', enuls);

```

```
// your domains
const _domain = "enulsid.enuls";
	
// resolve domain to get the address of the owner.
const owner = await sdk.getOwner(_domain);

console.log(owner);

// your address
const _address = "0x5aEa3F3f358347Abf94B554389174F966faeEfbB";

// get a domain default from a user's address, requiring the user to set the default domain name initially.
const domain = await sdk.getDomain(_address);

console.log(domain);
```

Thanks!
