# Macbook Touchbar Crypto Price Ticker
A touch bar widget for crypto currency price (Bitcoin, Ethereum, and Litecoin)
<p align="center">
<img src="https://github.com/jimmyadg/crypto_touchbar/blob/master/banner.JPG" width="400"/>
</p>

## Dependencies
- Install BetterTouchBarTool - https://www.boastr.net/downloads/
- Install jq  - brew install jq
- Download - touchbar_crypto.json https://github.com/jimmyadg/crypto_touchbar/blob/master/touchbar_crypto.json

## Installation
Launch BetterTouchBarTool and go to Preferences, click Manage Presets ,and simply import touchbar_crypto.json into BetterTouchBarTool. Enjoy!

## Configuration
Bitcoin and Ethereum prices are both from Gemini exchange, and Litcoin price is from Bitstamp exchange.
<br>
<br>
I am using the web api by cryptocompare.com, which you can easily edit the api url in the widgets and point to your desire exchange and fiat currency by editing COIN and EXCHANGE in the url below

https://min-api.cryptocompare.com/data/price?fsym=COIN&tsyms=USD&e=EXCHANGE

## Integrating Other Coins
Adding price ticker for other coin is easy
<br>
<br>
Simply click the +Widget button in BetterTouchBarTool's Preferences and assign the widget to "Run Apple Script and Show Return Value"
<br>
<br>
If you are unfamiliar with Apple Script, you can copy and paste the template code below and follow the configuration section to assign the widge to your desired coin.

<code>
set p to do shell script "curl 'https://min-api.cryptocompare.com/data/price?fsym=BTC&tsyms=USD&e=Gemini' | /usr/local/bin/jq .USD"
return "$" & p
</code>
