# Listing Inscription for Auction

Here is what the header should look like when listing an inscription for auction:

```
{
    "previousTx": "",
    "action": "auction",
    "timestamp": number,
    "data": {

    },
    "signature": "SHA3-512 hash of signature of previousTx + action + timestamp + data"
}
```

This is what the data field should look like:

```
"data": {
    "startingPrice": number, // The starting price in satoshis
    "payTo": "", // The address that the payment must be given to after the auction is completed
    "blocks": number, // How many blocks have to pass before the auction is completed.
    "blocksToPay": number // How many blocks the auction winner has to pay. If no one submits a bid or the highest bidder dosn't pay in time and there are no more bidders left, then the aution is cancelled.
}
```