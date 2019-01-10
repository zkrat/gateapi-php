# GateApi
APIv4 futures provides all sorts of futures trading operations. There are public APIs to retrieve the real-time market statistics, and private APIs which needs authentication to trade on user's behalf.

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: 1.1.0
- Package version: 1.1.0
- Build package: org.openapitools.codegen.languages.PhpClientCodegen
For more information, please visit [https://gate.io/page/contacts](https://gate.io/page/contacts)

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/gateio/GateApi.git"
    }
  ],
  "require": {
    "gateio/GateApi": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/GateApi/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$config = new GateApi\Api\Configuration("YOUR_API_KEY", "YOUR_API_SECRET");
$apiInstance = new GateApi\Api\FuturesApi(null, $config)
$order_id = '12345'; // string | ID returned on order successfully being created

try {
    $result = $apiInstance->cancelOrder($order_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FuturesApi->cancelOrder: ', $e->getMessage(), PHP_EOL;
}

?>
```

## Documentation for API Endpoints

All URIs are relative to *https://fx-api.gateio.io/api/v4*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*FuturesApi* | [**cancelOrder**](docs/Api/FuturesApi.md#cancelorder) | **DELETE** /futures/orders/{order_id} | Cancel a single order
*FuturesApi* | [**cancelOrders**](docs/Api/FuturesApi.md#cancelorders) | **DELETE** /futures/orders | Cancel all &#x60;open&#x60; orders matched
*FuturesApi* | [**createOrder**](docs/Api/FuturesApi.md#createorder) | **POST** /futures/orders | Create a futures order
*FuturesApi* | [**getMyTrades**](docs/Api/FuturesApi.md#getmytrades) | **GET** /futures/my_trades | List personal trading history
*FuturesApi* | [**getOrder**](docs/Api/FuturesApi.md#getorder) | **GET** /futures/orders/{order_id} | Get a single order
*FuturesApi* | [**listFuturesAccounts**](docs/Api/FuturesApi.md#listfuturesaccounts) | **GET** /futures/accounts | Query futures account
*FuturesApi* | [**listFuturesCandlesticks**](docs/Api/FuturesApi.md#listfuturescandlesticks) | **GET** /futures/candlesticks | Get futures candlesticks
*FuturesApi* | [**listFuturesContracts**](docs/Api/FuturesApi.md#listfuturescontracts) | **GET** /futures/contracts | List all futures contracts
*FuturesApi* | [**listFuturesFundingRateHistory**](docs/Api/FuturesApi.md#listfuturesfundingratehistory) | **GET** /futures/funding_rate | Funding rate history
*FuturesApi* | [**listFuturesInsuranceLedger**](docs/Api/FuturesApi.md#listfuturesinsuranceledger) | **GET** /futures/insurance | Futures insurance balance history
*FuturesApi* | [**listFuturesOrderBook**](docs/Api/FuturesApi.md#listfuturesorderbook) | **GET** /futures/order_book | Futures order book
*FuturesApi* | [**listFuturesTickers**](docs/Api/FuturesApi.md#listfuturestickers) | **GET** /futures/tickers | List futures tickers
*FuturesApi* | [**listFuturesTrades**](docs/Api/FuturesApi.md#listfuturestrades) | **GET** /futures/trades | Futures trading history
*FuturesApi* | [**listOrders**](docs/Api/FuturesApi.md#listorders) | **GET** /futures/orders | List futures orders
*FuturesApi* | [**listPositionClose**](docs/Api/FuturesApi.md#listpositionclose) | **GET** /futures/position_close | List position close history
*FuturesApi* | [**listPositions**](docs/Api/FuturesApi.md#listpositions) | **GET** /futures/positions | List all positions of a user
*FuturesApi* | [**updatePositionLeverage**](docs/Api/FuturesApi.md#updatepositionleverage) | **POST** /futures/positions/{contract}/leverage | Update position leverage
*FuturesApi* | [**updatePositionMargin**](docs/Api/FuturesApi.md#updatepositionmargin) | **POST** /futures/positions/{contract}/margin | Update position margin
*FuturesApi* | [**updatePositionRiskLimit**](docs/Api/FuturesApi.md#updatepositionrisklimit) | **POST** /futures/positions/{contract}/risk_limit | Update position risk limit


## Documentation For Models

 - [Contract](docs/Model/Contract.md)
 - [FundingRateRecord](docs/Model/FundingRateRecord.md)
 - [FuturesAccount](docs/Model/FuturesAccount.md)
 - [FuturesCandlestick](docs/Model/FuturesCandlestick.md)
 - [FuturesOrder](docs/Model/FuturesOrder.md)
 - [FuturesOrderBook](docs/Model/FuturesOrderBook.md)
 - [FuturesOrderBookItem](docs/Model/FuturesOrderBookItem.md)
 - [FuturesTicker](docs/Model/FuturesTicker.md)
 - [FuturesTrade](docs/Model/FuturesTrade.md)
 - [InsuranceRecord](docs/Model/InsuranceRecord.md)
 - [MyFuturesTrade](docs/Model/MyFuturesTrade.md)
 - [Position](docs/Model/Position.md)
 - [PositionClose](docs/Model/PositionClose.md)
 - [PositionCloseOrder](docs/Model/PositionCloseOrder.md)


## Author

support@mail.gate.io


