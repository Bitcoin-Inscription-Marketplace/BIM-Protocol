# Sending Offer for Inscription

Here is what the header should look like when sending an offer for an inscription:

```
{
    "rootTx": "",
    "action": "offer",
    "timestamp": number,
    "data": {

    }
}
```

This is what the data field should look like:

```
"data": {
    "offerPrice": number, // The price in satoshis that you are offering to pay for the inscription
    "offerFrom": "address" // The wallet making the offer
}
```