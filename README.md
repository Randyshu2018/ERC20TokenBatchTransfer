
```
npm install git://github.com/npm/npm.git#v1.0.27
```


```js
var transfer = require('../index.js')

transfer.init({
    senderAddress: "senderAddress",
    privateKey: "your senderAddress privateKey",
    contractAddress: "your erc20 contranct",
    provider: "https://ropsten.infura.io"
});

// formate:[{to:"receiver's address",amount:"amount to send"}]
transfer.batchTransfer([
    {to: "0xf7171d1ea98f698e22ef0ebfb5498d0c2ca83890", amount: 10},
    {to: "0xf7171d1ea98f698e22ef0ebfb5498d0c2ca83890", amount: 10},
    {to: "0xf7171d1ea98f698e22ef0ebfb5498d0c2ca83890", amount: 10},
    {to: "0xf7171d1ea98f698e22ef0ebfb5498d0c2ca83890", amount: 10},
    {to: "0xf7171d1ea98f698e22ef0ebfb5498d0c2ca83890", amount: 10},
    {to: "0xf7171d1ea98f698e22ef0ebfb5498d0c2ca83890", amount: 10}
]).then(function (result) { // return all transaction hash
    console.info(result)
});
```