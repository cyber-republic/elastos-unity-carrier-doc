---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - Usage

toc_footers:
  # - <a href='#'>Sign Up for a Developer Key</a>

includes:
  # - errors

search: true
---

# Introduction

Welcome to the React Native Elastos Carrier Bridges! You can use our bridges in javascript to access Elastos Carrier Core RPC endpoints, which can interact with Elastos Blockchain.

You can view usage in the dark area to the right.

# Carrier Bridges

## GetVersion

```javascript
static getVersion(){
  return exec('getVersion');
}
```
<!-- > Output Example:
```javascript
cry mechanic bean they discover vendor couple adapt walk room edit dinner
``` -->

This bridge returns a new mnemonic to create a new wallet.

## ImportWalletWithMnemonic

```javascript
import RNElastosMainchain from 'react-native-elastos-wallet-core';

RNElastosMainchain.ImportWalletWithMnemonic(mnemonic, (err, res) => {
  console.log(res); //expect "success"
});
```

This bridge imports existing wallet using its mnemonic. Every wallet have its mnemonic so you can import any wallet you already created in web wallet or everywhere.

### Parameters

Parameter | Description
--------- | -----------
mnemonic | mnemonic of the wallet you're going to import

