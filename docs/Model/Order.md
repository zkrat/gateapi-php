# # Order

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Order ID | [optional] [readonly] 
**text** | **string** | User defined information. If not empty, must follow the rules below:  1. prefixed with &#x60;t-&#x60; 2. no longer than 28 bytes without &#x60;t-&#x60; prefix 3. can only include 0-9, A-Z, a-z, underscore(_), hyphen(-) or dot(.) | [optional] 
**create_time** | **string** | Creation time of order | [optional] [readonly] 
**update_time** | **string** | Last modification time of order | [optional] [readonly] 
**create_time_ms** | **int** | Creation time of order (in milliseconds) | [optional] [readonly] 
**update_time_ms** | **int** | Last modification time of order (in milliseconds) | [optional] [readonly] 
**status** | **string** | Order status  - &#x60;open&#x60;: to be filled - &#x60;closed&#x60;: filled - &#x60;cancelled&#x60;: cancelled | [optional] [readonly] 
**currency_pair** | **string** | Currency pair | 
**type** | **string** | Order type. limit - limit order | [optional] [default to 'limit']
**account** | **string** | Account type. spot - use spot account; margin - use margin account; cross_margin - use cross margin account. Portfolio margin account must set to &#x60;cross-margin&#x60; | [optional] [default to 'spot']
**side** | **string** | Order side | 
**amount** | **string** | Trade amount | 
**price** | **string** | Order price | 
**time_in_force** | **string** | Time in force  - gtc: GoodTillCancelled - ioc: ImmediateOrCancelled, taker only - poc: PendingOrCancelled, makes a post-only order that always enjoys a maker fee - fok: FillOrKill, fill either completely or none | [optional] [default to 'gtc']
**iceberg** | **string** | Amount to display for the iceberg order. Null or 0 for normal orders. Set to -1 to hide the order completely | [optional] 
**auto_borrow** | **bool** | Used in margin or cross margin trading to allow automatic loan of insufficient amount if balance is not enough. | [optional] 
**auto_repay** | **bool** | Enable or disable automatic repayment for automatic borrow loan generated by cross margin order. Default is disabled. Note that:  1. This field is only effective for cross margin orders. Margin account does not support setting auto repayment for orders. 2. &#x60;auto_borrow&#x60; and &#x60;auto_repay&#x60; cannot be both set to true in one order. | [optional] 
**left** | **string** | Amount left to fill | [optional] [readonly] 
**fill_price** | **string** | Total filled in quote currency. Deprecated in favor of &#x60;filled_total&#x60; | [optional] [readonly] 
**filled_total** | **string** | Total filled in quote currency | [optional] [readonly] 
**fee** | **string** | Fee deducted | [optional] [readonly] 
**fee_currency** | **string** | Fee currency unit | [optional] [readonly] 
**point_fee** | **string** | Points used to deduct fee | [optional] [readonly] 
**gt_fee** | **string** | GT used to deduct fee | [optional] [readonly] 
**gt_discount** | **bool** | Whether GT fee discount is used | [optional] [readonly] 
**rebated_fee** | **string** | Rebated fee | [optional] [readonly] 
**rebated_fee_currency** | **string** | Rebated fee currency unit | [optional] [readonly] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)
