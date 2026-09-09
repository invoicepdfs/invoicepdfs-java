

# DocumentComplianceRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**documentType** | [**DocumentTypeEnum**](#DocumentTypeEnum) |  |  [optional] |
|**data** | [**DocumentInvoiceDataInput**](DocumentInvoiceDataInput.md) |  |  |
|**profile** | **String** | Which ruleset to hold the document to. Rulesets differ: a document valid under one can be rejected by another, so there is no default. |  |



## Enum: DocumentTypeEnum

| Name | Value |
|---- | -----|
| INVOICE | &quot;invoice&quot; |
| CREDIT_NOTE | &quot;credit_note&quot; |
| DEBIT_NOTE | &quot;debit_note&quot; |
| QUOTE | &quot;quote&quot; |
| RECEIPT | &quot;receipt&quot; |
| PROFORMA | &quot;proforma&quot; |
| PURCHASE_ORDER | &quot;purchase_order&quot; |
| DELIVERY_NOTE | &quot;delivery_note&quot; |



