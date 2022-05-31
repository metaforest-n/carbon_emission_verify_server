# Introduction

### Main functions:

- Server counts the gas cost of each account transactions on the blockchain in every 6600 block heights, and calculates the WEB3 carbon emissions of each account, according to the carbon emission calculation standard (account carbon emission = Account gas cost/Total gas cost of the entire network * Electric power consumption of the entire network \* Carbon emissions per unit of electric power consumption), Currently it is MOCK processing;
- Using Admin account of CarbonEmission contract to record every account's carbon emission into contract.
- Count walking kilometers of users, calculating the carbon reduction in the account according to calculation standard;
- Using the Admin account of the CarbonEnergy contract, mint CET to the user according to the user's carbon reduction;

### TODO

- Authentication logic through SIWE (Sign-In with Ethereum)
- Security protection of the interface. e.g. replay attack
- More

### Environment

Nodejs > 14

If use **Node.js >= 16.10 **
then use **yarn**
otherwise use **npm**

### Config

`.env` file

- `PRIVATE_KEY`: The real implementation is an automated private key escrow service providing private keys
- `JSON_RPC`: test chain http rpc for this event
- `ENERGY_ADDRESS`: carbon credit contract address
- `EMISSION_ADDRESS`: carbon emission contract address

### initialization

```
yarn install // install dependencies
```

or

```
npm install
```

#### run

```
yarn start // http://localhost:3000
```

or

```
npm run start
```
