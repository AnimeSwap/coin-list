# How to add to this coin list

1. fork repo
2. append coin info to chain `.js` file (such as `aptos/devnet.js`)
3. add icon to `icons` folder
4. Pull Request

Coin Info example:

```javascript
{
  address: '0x1::aptos_coin::AptosCoin',
  decimals: 8,
  symbol: 'APT',
  name: 'Aptos',
  logoURL: 'https://coinlist.animeswap.org/icons/APT.svg',
  projectURL: 'https://aptoslabs.com/',
}
```

```javascript
{
  address: '0x16fe2df00ea7dde4a63409201f7f4e536bde7bb7335526a35d05111e68aa322c::TestCoinsV1::USDT',
  decimals: 8,
  symbol: 'USDT',
  name: 'Tether USD',
  logoURL: 'https://coinlist.animeswap.org/icons/USDT.webp',
  extensions: {
    stableUSD: true,
  },
}
```

Coin Schema:
```typescript
class Coin {
  address: string
  decimals: number
  symbol: string
  name: string
  logoURL?: string
  projectURL?: string
  extensions?: object
}
```

* `address`: the address of the coin on blockchain
* `decimals`: the decimals of the coin
* `symbol`: globally unique symbol within this coin registry
* `logoURL`: optional, the URL of the logo of the coin
* `projectURL`: optional, the project website of the coin
* `extensions`: optional, used for special extra data
