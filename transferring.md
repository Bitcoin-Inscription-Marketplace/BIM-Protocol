# Transferring Inscription to Another Wallet

Here is what the header should look like when transferring a BIM inscription:

```
{
    "rootTx": "",
    "action": "send",
    "timestamp": number,
    "data": {

    },
    "signature": "SHA3-512 hash of signature of rootTx + action + timestamp + data"
}
```

Here is what the data field should look like:

```
"data": {
    "sendTo": "" // The address to send the BIM inscription to
}
```