![image](https://github.com/Kelldotbtc/olorin-solana-spl-token-sniper-bot/assets/172572822/bd6c8c68-2706-4881-90e4-cfa811c0be72)


Features:

New Token Sniper 

- Snipe any new token using the token contract address as soon as the liquidity pool opens. This is faster than using a Telegram sniper like Unibot because you can use your own RPC endpoint rather than relying on a public endpoint.
- Set custom slippage amount default is set at 3000 bps.
- Set number of retries.
- Swap all feature allows the user to quickly and easily swap out of their entire position.
- Use your own RPC endpoint for better reliability and faster sniping (Free Helius RPC enpoint works great and is highly recommended).

Auto Sniper Bot

- Presets for bull, bear, and neutral market conditions. Simply press a button to load presets that give you a starting point for configuring your buy/sell parameters. All parameters can be manually adjusted to the user's liking.
- Default parameters include (details for each indicator below): Trailing Stop Trigger Price, Trailing Stop Percentage, Overall Stop Loss Percentage, Skip If Price Drops Percentage, Volume 24h, Liquidity (USD), Price Change % (5m,1h,6h,24h), and Max Positions.
- Additional parameters such as Mean Reversion Buying Strategy using RSI and MACD calculations can be unlocked with a Birdeye API key (not free). 
- Automatically fetches Top 150 Tokens (by 24h Volume), Top 50 Trending Tokens, and 50 Most Recently Minted Tokens. This feature is supported by our servers so an API key is NOT needed.
- Token Security Check. All tokens are checked against the Solana SPL-Token API to ensure Mint Authority and Freeze Authority have been revoked. Tokens that have not had both of these authorities revoked are skipped due to the high likelihood of rugpulling. This feature does not require an API key from the user since it only requires the default Solana endpoint.
- Token Technical Analysis is conducted periodically on your token list so that tokens in the list are sniped as soon as your buying criteria are met.
- Price monitoring. Open positions are monitored for price changes every minute and as soon as the token price hits one of your sell thresholds the bot quickly sells out of your entire position for you utilizing your trailing stop settings.
- Manual Token List - Build your own token list by simply listing the token contract addresses one per line in the swap.txt file.
- Use your own RPC endpoint for better reliability and faster sniping (Free Helius RPC enpoint works great and is highly recommended).
- Future features coming soon. We're always builing to make this product even better!

Installation

- Download the Zip file and unzip to your desired location.
- Unzip _internal.zip library using winrar. When finished all files should be located inside the _internal directory except for Olorin_GUI.exe, LICENSE, and README.md
- Run the Olorin_GUI.exe
- On initial startup your configuration and tokens.txt files will automatically be created. This configuration file stores your settings each time you close the sniper so the next time you restart your settings are the same. The swap.txt file will contain the token addresses of tokens you want to auto-snipe.

Quick Start Instructions

- Create a new wallet (Backpack Recommended)
- Fund the new wallet with some SOL
- Copy the private key and paste it into the Wallet Private Key Field in Olorin using ctl+c/ctrl+v.
- Go to Helius and get your free RPC endpoint (optional but recommended).
- You can now use the Manual Sniper to buy/swap tokens. The manual sniper is available for anyone to use.
- To use the Auto-Sniper features you will need to hold 10,000 $OLO (CA: HKGb5t1LPKGL4vLB4Hf4LqaW26EtCpGPdRgWS6LUasqT) in the same wallet connected to Olorin. The default CA in the Swap To Token field is the Olorin contract address so you can easily purchase the tokens from the sniper or as an alternative you can get $OLO on Raydium or Jupiter.
- Olorin is now ready to use! Feel free to fetch tokens from our database using one of the fetch tokens buttons or build your own list by manually adding token contract addresses to the swap.txt file (in the same directory as Olorin).

Auto-Sniper Parameters
- Base Token Address - This is the contract address the auto-sniper will use to swap from and back to when a position is opened/closed. The default token is SOL and this cannot be changed at this time - Future integrations will allow swapping from other tokens.
- Amount of Base Token - The amount of the base token you want the auto-sniper to use for each token swap. For example: 0.10 SOL per newly opened position.
- RSI Time Period - Used only with Birdeye API trading strategy. This is used to caluculate RSI based on the number of periods the user prefers to use. If you aren't familiar with how RSI is caluclated you should read more about it before changing the default setting.
- MACD Time Period = Used only with Birdeye API trading strategy. These settings are for MACD slow,fast, and trigger moving averages to help determine when a trend turns bullish and when the indicator should trigger a buy/swap.
- RSI Buy Threshold - The RSI threshold that will trigger a buy.
- MACD Buy Threshold - The MACD threshold that will trigger a buy.
- Trailing Stop Trigger Price - The percentage of the initial price paid for a token when the bot should start the trailing stop feature. For example if the setting is 1.2 then this will be triggered when the token price reaches 20% above the initial purchase price.
- Trailing Stop Percentage - This is the percentage the price needs to fall to trigger a sell after the Trailing Stop Trigger Price is reached. For example if the token reaches 1.2% of the token price as in the example above, the position will be sold if the price drops by 2% within the next 60 seconds. If the price continues to increase, a sell will not engage until a 2% drop occurs. This is to help lock in higer profits and to prevent selling out of a position prematurely.
- Overall Stop Loss Percentage - The percentage below the initial token purchase price you want the bot to sell out of an open position. For example a setting of 0.4 means if the token price drops below 40% of the initial purchase price, the bot will automatically sell the position to avoid a complete loss.
- Skip If Price Drops Percentage - The percentage at which a token in loss should not be sold. For example a setting of 0.20 means that if the token suddenly drops below 20% of it's initial purchase price, the bot will keep the position open to sell later when/if the token price recovers.
- Historical Data Period (days) - This is part of the Birdeye API trading strategy and requires an API key. This setting is the number of periods to look at for calculating RSI and MACD in Days.
- Volume 24h - This is the minimum 24 hour volume a token should have before the bot considers it for a trade.
- Liquidity USD - This is the minimum liquidity a token should have before the bot will consider trading it.
- Price Change Percentage (5m,1h,6h,24h) - The price increase a token should have over the specified periods of time before the bot will consider trading it.
- Max Positions - The maximum number of positions the bot should have open at any given time. The bot will stop further Technical Analysis (TA) until the number of open positions falls below this number.

Bot Fees
- 0.001 SOL per trade fixed fee is added. This helps pay server costs and allows us to further develope this product.

NOTE: Trading using this bot requires market knowledge and if the bot snipes a token it should not be considered safe or a good trade. Olorin is simply a tool to help traders profit but it in no way guarantees returns. As always, you should do your own research before making any trades in this highly volatile market. This being said, we wish you the best of luck and hope you enjoy this product! Please join our community on Telegram and leave your feedback. We love hearing from our users! Telegram: t.me/olorinpub
