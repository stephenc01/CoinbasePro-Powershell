## Powershell Module for accessing the Coinbase Pro currency exchange API. 

#### Install (Requires PowerShellGet)
> Install-Module -Name CoinbasePro-Powershell

#### Usage 

###### Public Requests
* Get-CoinbaseProProducts - Gets a list of all tradable products on the exchange
* Get-CoinbaseProCurrencies - Lists all currencies on the exchange
* Get-CoinbaseProTime - Gets current time on the exchange
* Get-CoinbaseProProductOrderBook - Gets a list of the orders on the order book for a specific product
* Get-CoinbaseProProductTicker - Gets ticker information for a specific product
* Get-CoinbaseProProductTrades - Get a list of recent trades for a specific product
* Get-CoinbaseProProductStats - Lists stats about a specific product

###### Authenticated Requests
* Get-CoinbaseAccounts - Gets a list of your Coinbase accounts. *(Requires view or trade permission)*
* Get-CoinbaseProAccounts - Gets a list of your Coinbase Pro accounts or specify a specific account to query. *(Requires view or trade permission)*
* Get-CoinbaseProAccountHistory - Lists the history of a specific account ID (Paginated) *(Requires view or trade permission)*
* Get-CoinbaseProAccountHolds - Lists funds on hold on a specific account ID *(Requires view or trade permission)*
* Get-CoinbaseProFills - Lists orders which have filled on a specific account ID (Paginated). *(Requires view or trade permission)*
* Get-CoinbaseProOrder - Lists order status for specific order. *(Requires view or trade permission)*
* Get-CoinbaseProOrders - Lists orders for specific product (Paginated). *(Requires view or trade permission)*
* Get-CoinbaseProFees - Lists taker & maker fees as well as 30 day trailing volume.
* New-CoinbaseProLimitOrder - Creates a new limit order for a product. *(Requires trade permission)*
* New-CoinbaseProMarketOrder - Creates a new market order for a product. *(Requires trade permission)*
* New-CoinbaseProStopOrder - Creates a new stop order for a product. *(Requires trade permission)*
* Remove-CoinbaseProOrder - Cancels a specific order or all orders if no ID is specified for the specified product. *(Requires trade permission)*
* Get-CoinbaseProPaymentMethods - Gets list of payment methods listed in Coinbase Pro *(Requires transfer permission)*
* Invoke-CoinbaseProWithdrawal - Withdraws funds from selected currency to a payment method, coinbase account or crypto address. *(Requires transfer permission)*
* Invoke-CoinbaseProDeposit - Deposit funds from payment method or coinbase account. *(Requires transfer permission)*


#### Authenticating with API key
Keys and secrets are only stored in memory and should be passed to the module when running commands. 
Editing PSDefaultParameterValues can be a useful way of passing the API details to the module.

>$PSDefaultParameterValues = @{"\*Coinbase\*:APIKEY" = "KEYHERE";"\*Coinbase\*:APIPHRASE" = "PHRASEHERE";"\*Coinbase\*:APISECRET" = "SECRETHERE"}