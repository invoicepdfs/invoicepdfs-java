

# StandardLineItemInput

A fully priced line: unit, price, tax, discount and SKU.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** |  |  |
|**description** | **String** |  |  [optional] |
|**quantity** | **String** | Decimal string |  |
|**unitPrice** | **String** | Decimal string, major units |  [optional] |
|**unit** | **String** |  |  [optional] |
|**sku** | **String** |  |  [optional] |
|**discount** | [**LineItemDiscountInput**](LineItemDiscountInput.md) |  |  [optional] |
|**taxes** | [**List&lt;LineItemTaxInput&gt;**](LineItemTaxInput.md) |  |  [optional] |



