# ERC20 Token

[![NPM Package](https://img.shields.io/npm/v/@vittominacori/erc20-token.svg?style=flat-square)](https://www.npmjs.com/package/@vittominacori/erc20-token)
[![CI](https://github.com/vittominacori/erc20-token/workflows/CI/badge.svg?branch=master)](https://github.com/vittominacori/erc20-token/actions/)
[![Coverage Status](https://coveralls.io/repos/github/vittominacori/erc20-token/badge.svg?branch=master)](https://coveralls.io/github/vittominacori/erc20-token?branch=master)
[![MIT licensed](https://img.shields.io/github/license/vittominacori/erc20-token.svg)](https://github.com/vittominacori/erc20-token/blob/master/LICENSE)

A simple Smart Contract for a Standard, Capped, Mintable, Burnable, Payable ERC20 Token.

Token has a Role Based Access Control so you can add the `MINTER` permission to users or Smart Contracts.

Token has a `trasferEnabled` property. Nobody can transfer tokens until the property will be enabled or you can define users as `OPERATOR` allowed to transfer also if not enabled.

Token has the ERC1363 behaviors. [ERC1363](https://eips.ethereum.org/EIPS/eip-1363) is an ERC20 compatible token that can make a callback on the receiver contract to notify token transfers or token approvals.

## Install

```bash
npm install @vittominacori/erc20-token
```

## Usage

```solidity
pragma solidity ^0.7.0;

import "@vittominacori/erc20-token/contracts/ERC20Base.sol";

contract MyToken is ERC20Base {

    constructor (
        string memory name,
        string memory symbol,
        uint8 decimals,
        uint256 cap,
        uint256 initialSupply,
        bool isTransferEnabled
    ) ERC20Base(name, symbol, decimals, cap, initialSupply, isTransferEnabled) {}

  // your stuff
}
```

## Development

### Install dependencies

```bash
npm install
```

### Usage (using Truffle)

Open the Truffle console

```bash
npm run truffle:console
```

#### Compile

```bash
npm run truffle:compile
```

#### Test

```bash
npm run truffle:test
```

### Usage (using Hardhat)

Open the Hardhat console

```bash
npm run hardhat:console
```

#### Compile

```bash
npm run hardhat:compile
```

#### Test

```bash
npm run hardhat:test
```

#### Code Coverage

```bash
npm run hardhat:coverage
```

## Linter

Use Solhint

```bash
npm run lint:sol
```

Use ESLint

```bash
npm run lint:js
```

Use ESLint and fix

```bash
npm run lint:fix
```

## License

Code released under the [MIT License](https://github.com/vittominacori/erc20-token/blob/master/LICENSE).
