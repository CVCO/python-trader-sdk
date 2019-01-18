# Setup

1. Clone this project from the git repo.
2. At project root, install this package by running  
   `$ pip install .`

# Usage

```python
from bincentive_trader.client import TraderClient

email = 'me@example.com'
password = 'super secret'

client = TraderClient(email, password, False)

```

Available clients methods are:
- get_strategy_list(timeout=None)
- get_exchange_list(timeout=None)
- add_market_order(strategy_id, exchange_id, base_currency, quote_currency, side, amount, leverage=None, timeout=None)
- get_history_list(strategy_id, begin_time, end_time, account_type='real', timeout=None)
- add_api_key(api_key, api_secret_key, exchange_id, timeout=None)
- get_api_key_list(timeout=None)
- delete_api_key(exchange_id, timeout=None)

Each method has a `timeout` parameter that will cause a `bincentive_trader.exceptions.Timeout`
exception if no response is received in the specified seconds.

<a name="BincentiveClient"></a>

## Bincentive Client Methods
Bincentive Trader Client

**Kind**: global class  

* [BincentiveClient](#BincentiveClient)
    
    * [.addOrder(strategyId, exchangeId, baseCurrency, quoteCurrency, orderType, orderSide, unit, limitPrice)](#BincentiveClient+addOrder)
    * [.getHistoryList()](#BincentiveClient+getHistoryList)
    * [.getStrategyList()](#BincentiveClient+getStrategyList)
    * [.getExchangeList()](#BincentiveClient+getExchangeList)
    * [.addApiKey(apiKey, secretKey, exchangeId, apiNickname, fixApiAssign)](#BincentiveClient+addApiKey)
    * [.deleteApiKey(exchangeId)](#BincentiveClient+deleteApiKey)
    * [.getApiKeyList()](#BincentiveClient+getApiKeyList)

<a name="new_BincentiveClient_new"></a>

<a name="BincentiveClient+addOrder"></a>

### bincentiveClient.addOrder(strategyId, exchangeId, baseCurrency, quoteCurrency, orderType, orderSide, unit, limitPrice)
Adds an order for a specific strategy

**Kind**: instance method of [<code>BincentiveClient</code>](#BincentiveClient)  

| Param | Type |
| --- | --- |
| strategyId | <code>number</code> | 
| exchangeId | <code>number</code> | 
| baseCurrency | <code>string</code> | 
| quoteCurrency | <code>string</code> | 
| orderType | <code>string</code> | 
| orderSide | <code>string</code> | 
| unit | <code>number</code> | 
| limitPrice | <code>number</code> | 

<a name="BincentiveClient+getHistoryList"></a>

### bincentiveClient.getHistoryList()
Gets the historical data of all transactions

**Kind**: instance method of [<code>BincentiveClient</code>](#BincentiveClient)  


<a name="BincentiveClient+getStrategyList"></a>

### bincentiveClient.getStrategyList()
Gets the list of strategies

**Kind**: instance method of [<code>BincentiveClient</code>](#BincentiveClient)  
 
<a name="BincentiveClient+getExchangeList"></a>

### bincentiveClient.getExchangeList()
Gets the list of exchanges 

**Kind**: instance method of [<code>BincentiveClient</code>](#BincentiveClient)  
<a name="BincentiveClient+addApiKey"></a>

### bincentiveClient.addApiKey(apiKey, secretKey, exchangeId, apiNickname, fixApiAssign)
Adds all the keys of each transaction

**Kind**: instance method of [<code>BincentiveClient</code>](#BincentiveClient)  

| Param | Type |
| --- | --- |
| apiKey | <code>string</code> | 
| secretKey | <code>string</code> | 
| exchangeId | <code>number</code> | 
| apiNickname | <code>string</code> | 
| fixApiAssign | <code>boolean</code> | 

<a name="BincentiveClient+deleteApiKey"></a>

### bincentiveClient.deleteApiKey(exchangeId)
Deletes all the keys of a transaction

**Kind**: instance method of [<code>BincentiveClient</code>](#BincentiveClient)  

| Param | Type |
| --- | --- |
| exchangeId | <code>number</code> | 

<a name="BincentiveClient+getApiKeyList"></a>

### bincentiveClient.getApiKeyList()
Gets API key list

**Kind**: instance method of [<code>BincentiveClient</code>](#BincentiveClient)  


