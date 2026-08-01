

# DocumentOut


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** |  |  |
|**documentType** | [**DocumentTypeEnum**](#DocumentTypeEnum) |  |  |
|**number** | **String** |  |  |
|**status** | **String** |  |  |
|**issueDate** | **LocalDate** |  |  |
|**dueDate** | **LocalDate** |  |  [optional] |
|**currency** | **String** |  |  |
|**locale** | **String** |  |  [optional] |
|**businessProfileId** | **String** |  |  |
|**customerId** | **String** |  |  |
|**sourceDocumentId** | **String** |  |  [optional] |
|**reason** | **String** |  |  [optional] |
|**data** | **Map&lt;String, Object&gt;** |  |  |
|**totals** | [**InvoiceTotalsOut**](InvoiceTotalsOut.md) |  |  |
|**createdAt** | **String** |  |  |
|**updatedAt** | **String** |  |  |
|**finalizedAt** | **String** |  |  [optional] |



## Enum: DocumentTypeEnum

| Name | Value |
|---- | -----|
| INVOICE | &quot;invoice&quot; |
| CREDIT_NOTE | &quot;credit_note&quot; |
| QUOTE | &quot;quote&quot; |
| RECEIPT | &quot;receipt&quot; |
| PROFORMA | &quot;proforma&quot; |
| PURCHASE_ORDER | &quot;purchase_order&quot; |
| DELIVERY_NOTE | &quot;delivery_note&quot; |



