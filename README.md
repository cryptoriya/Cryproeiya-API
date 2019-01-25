CRYPTORIYA public API
All API requests are made from this address: ``` https://www.cryptoriya.io/exchange/home/info_trans/<pair listing>. Currency pairs are hyphen-separated (-), e.g.: https://www.cryptoriya.io/exchange/home/info_trans/eth_btc ```

You can use only one pair: https://www.cryptoriya.io/exchange/home/info_trans/eth_btc. A set of pairs works with all the methods presented in the public api except info. All information is cached every 2 seconds, so there's no point in making more frequent requests. All API responses have the following format JSON.

Important! API will display an error if we disable one of the pairs listed in your request. 

Method info
This method provides all the information about currently active pairs, such as the minimum price, the maximum price, the minimum transaction size, the commission for each pair.

Sample request: https://www.cryptoriya.io/exchange/home/info
Sample response:

```
{
  "server_time": 1548436749,
  "pairs": {
    "eth_btc": {
      "min_deposit": "0.1",
      "max_deposit": "210",
      "min_total": 0.0029144619374897,
      "fee": "10"
    },
```

min_price: minimum price allowed during trading.

max_price: maximum price allowed during trading.

min_amount: minimum buy transaction size.

fee: commission for this pair.

<b><h2>Method info</h2><b>

This method provides all the information about currently active pairs, such as: the maximum price, the minimum price, average price, trade volume, trade volume in currency, the last trade, Buy and Sell price. All information is provided over the past 24 hours.

Sample request: https://www.cryptoriya.io/exchange/home/info_trans/eth_btc
Sample response:

```
{
  "eth_btc": {
    "vol_24": "5",
    "vol_30": "12057",
    "last": "5",
    "price_cur": 0.03237357745581,
    "price_last": 0.030963,
    "updated": 1548346235
  }
}
```

vol_24: 24 hours trade volume.

vol_30: 30 days trade volume in currency.

last: the last trade volume.

price_cur: current price.

price_last: Last tread price

updated: last update of cache.
