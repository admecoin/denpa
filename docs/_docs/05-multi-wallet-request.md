---
title: "Multi-Wallet Request"
permalink: /docs/request/multi-wallet/
excerpt: "Making multi-wallet request via laravel-playcoinrpc."
classes: wide
---
Since [version 1.2.4]({{ 'release/1.2.4' | relative_url }}), the package supports multi-wallet requests as described in [Release Notes](https://playcoin.org/en/release/v0.15.0.1#multi-wallet-support) for Playcoin Core v0.15.0.1.

### Altcoin support
Altcoins that forked after or include [PR 8694](https://github.com/playcoin/playcoin/pull/8694/files) and [PR 10849](https://github.com/playcoin/playcoin/pull/10849) should support multi-wallet calls made via this package.

### Making request
To make multi-wallet request, you'll need to use `wallet($filename)` method to specify wallet file name.
```php
$balance = playcoind()
    ->wallet('wallet2.dat')
    ->getBalance();

echo $balance->get();
```
