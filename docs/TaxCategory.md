

# TaxCategory

How a tax is treated, as opposed to what it is called.  `name` and `rate` do not say this: two taxes at 0% may be zero-rated, exempt, reverse-charge or outside scope, and EN 16931 keeps them in separate VAT breakdown groups with different mandatory fields. Optional, so an invoice that never mentions a category calculates exactly as before.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**code** | **String** | UNCL5305 tax category code — S standard, Z zero-rated, E exempt, AE reverse charge, K intra-community, G export, O outside scope |  |
|**exemptionReason** | **String** |  |  [optional] |
|**exemptionReasonCode** | **String** |  |  [optional] |



