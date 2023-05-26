# BIM - Bitcoin Inscription Marketplace

The protocol may change in the future! Do not build anything that you may lose money on using this protocol yet until it is in a more completed state. I am not responsible for any lost funds.

## Why use BIM over Ordinals

* BIM doesn't need a wallet that provides satoshi control
* BIM makes selling, auctioning and other marketplace functions 100% decentralised, apart from letting others mint an inscription in a collection.
* Collections
* You can add BIM data to any transaction that you make, saving on tx fees
* If you can think of more, please create an issue!

## Disadvantages of BIM (compared to Ordinals)

* Higher transaction fees, if only transacting BIM data, or if compression doesn't reduce file size
* If you can think of more, please create an issue!

## Explanation of how BIM works

BIM uses a technology used in Bitcoin called SegWit. In simple terms, SegWit puts signature data outside of the main part of the transaction, to save block space. This allows a higher amount of data to be stored in a block, to be specific 4mb. SegWit also allows any data to be stored in the extra space. This is where BIM information is stored.

## Table of Contents

* [Header and Compression](header-compression.md)
* [Creating Inscription](creating-inscription.md)
* [Creating Collection](creating-collection.md)
* [Transferring Inscription to Another Wallet](transferring.md)
* [Listing Inscription for Sale](listing-sale.md)
* [Purchasing Inscription that is listed for Sale](purchasing-sale.md)
* [Listing Inscription for Auction](listing-auction.md)
* [Submit Bid in Auction](submit-bid.md)
* [Pay for Auction](pay-auction.md)
* Sending Offer for Inscription
* Accepting Offer
* Paying for Accepted Offer

## Since the previous tx can be set to anything, can BIM inscriptions be faked?

No, since wallets are expected to verfy everything. The previous tx is there for two reasons:
1. Speed up discovery AFTER verification
2. To be able to determine the root transaction, aka. the tx where the BIM is created