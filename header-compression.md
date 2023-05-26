# Header and Compression

## Header

The Header is what is included in every single transaction containing BIM data. Any valid JSON can be used and does NOT need to have the whitespace, unlike below. Here is an example header:

```
{
    "previousTx": "",  // The previous transaction hash that interacts with the BIM inscription. Not necessary if this is a collection creation or new inscription
    "action": "", // The action that is being performed. Possible values: createbim, createcoll, send, sell, auction, offer, acceptoffer, offerpayment, buy, bid, payauction
    "timestamp": number // The unix timestamp that the BIM inscription is created. Must be higher than the one in previousTx
    "data": {

    }, // The actual BIM data
    "signature": "" // The signature for verifing that the person performing the transaction has access to the private keys for the owner of the inscription or the person making the offer. Not required on createbim, buy and createcoll
}
```
"previousTx" is the last transaction that is performed on that BIM inscription. Eg. if the last transaction that contained the data was `b4f9b23bd3990b6ad042256dbf8642e474ad7469635daaacecb1826b3185d18a` then that is what would be put in this field. If the previous transaction that contains the BIM is a collection, then that should NOT be used as collections can contain many BIMS and software cannot determine the BIM owner.
"action" is what is being done. This must correspond with what is in the data field.
"data" is the actual BIM data. See the rest of the md files for more detail.
"signature" is what verifies that the person doing the transaction holds the private key to whoever the data corresponds to. The signature is created using th previousTx, action, timestamp and data concatenated, then hashed using SHA3-512. The signature is hashed to help reduce the block size.

## Compression

Compression is done with the highly popular, LZMA2. This is because LZMA2 is known for incredibly high compression ratios, sacrificing speed for file size, which is very important when storing data in a blockchain. Compression is a required part of the BIM protocol and if compression is not performed then it is NOT BIM compliant. Please note that LZMA2 may increase file sizes on rare circumstances.