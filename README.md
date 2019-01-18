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
    
    * [.add_market_order(strategy_id, exchange_id, base_currency, quote_currency, side, amount, leverage=None, timeout=None)](#BincentiveClient+add_market_order)
    * [.get_history_list(strategy_id, begin_time, end_time, account_type='real', timeout=None)](#BincentiveClient+get_history_list)
    * [.get_strategy_list(timeout=None)](#BincentiveClient+get_strategy_list)
    * [.get_exchange_list(timeout=None)](#BincentiveClient+get_exchange_list)
    * [.add_api_key(api_key, api_secret_key, exchange_id, timeout=None)](#BincentiveClient+add_api_key)
    * [.delete_api_key(exchange_id, timeout=None)](#BincentiveClient+delete_api_key)
    * [.get_api_key_list(timeout=None)](#BincentiveClient+get_api_key_list)

<a name="new_BincentiveClient_new"></a>

<a name="BincentiveClient+add_market_order"></a>

### bincentiveClient.add_market_order(strategy_id, exchange_id, base_currency, quote_currency, side, amount, leverage=None, timeout=None)
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

<a name="BincentiveClient+get_history_list"></a>

### bincentiveClient.get_history_list(strategy_id, begin_time, end_time, account_type='real', timeout=None)
Gets the historical data of all transactions

**Kind**: instance method of [<code>BincentiveClient</code>](#BincentiveClient)  


<a name="BincentiveClient+get_strategy_list"></a>

### bincentiveClient.get_strategy_list(timeout=None)
Gets the list of strategies

**Kind**: instance method of [<code>BincentiveClient</code>](#BincentiveClient)  
 
<a name="BincentiveClient+get_exchange_list"></a>

### bincentiveClient.get_exchange_list(timeout=None)
Gets the list of exchanges 

**Kind**: instance method of [<code>BincentiveClient</code>](#BincentiveClient)  
<a name="BincentiveClient+add_api_key"></a>

### bincentiveClient.add_api_key(api_key, api_secret_key, exchange_id, timeout=None)
Adds all the keys of each transaction

**Kind**: instance method of [<code>BincentiveClient</code>](#BincentiveClient)  

| Param | Type |
| --- | --- |
| apiKey | <code>string</code> | 
| secretKey | <code>string</code> | 
| exchangeId | <code>number</code> | 
| apiNickname | <code>string</code> | 
| fixApiAssign | <code>boolean</code> | 

<a name="BincentiveClient+delete_api_key"></a>

### bincentiveClient.delete_api_key(exchange_id, timeout=None)
Deletes all the keys of a transaction

**Kind**: instance method of [<code>BincentiveClient</code>](#BincentiveClient)  

| Param | Type |
| --- | --- |
| exchangeId | <code>number</code> | 

<a name="BincentiveClient+get_api_key_list"></a>

### bincentiveClient.get_api_key_list(timeout=None)
Gets API key list

**Kind**: instance method of [<code>BincentiveClient</code>](#BincentiveClient)  


