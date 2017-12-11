# New Macbook Touchbar Crypto Price Ticker
touch bar tool for crypto currency price (Bitcoin, Ethereum, and Litecoin)

<img style="display: block; margin: 0 auto; width:10%;" src="https://github.com/jimmyadg/crypto_touchbar/blob/master/ex.JPG" alt="imge"/>

## Dependencies
- Install BetterTouchBarTool - https://www.boastr.net/downloads/
- Install jq  - brew install jq
- Download - touchbar_crypto.json

##Install
Launch BetterTouchBarTool and go to Preferences, click Manage Presets ,and simply import touchbar_crypto.json into BetterTouchBarTool. Enjoy!

##Configuration
Bitcoin and Ethereum prices are both from Gemini exchange, and Litcoin price is from Bitstamp exchange. I am using the web api by cryptocompare.com, which you can easily edit the api url in the widgets and point to your desire exchange and fiat currency by editing COIN and EXCHANGE in the url below

https://min-api.cryptocompare.com/data/price?fsym=COIN&tsyms=USD&e=EXCHANGE
