# Submit Bid in Auction

Here is what the header should look like when submitting a bid into an auction:

```
{
    "rootTx": "",
    "action": "bid",
    "timestamp": number,
    "data": {

    }
}
```

This is what the data field should look like:

```
"data": {
    "bid": number, // The bid that you want. Must be higher than the previous bid
    "wallet": "" // The wallet submitting the bid
}
```