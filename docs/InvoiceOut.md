

# InvoiceOut


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** |  |  |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**invoiceNumber** | **String** |  |  |
|**documentType** | [**DocumentTypeEnum**](#DocumentTypeEnum) |  |  |
|**issueDate** | **LocalDate** |  |  |
|**dueDate** | **LocalDate** |  |  [optional] |
|**currency** | **String** |  |  |
|**locale** | **String** |  |  [optional] |
|**businessProfileId** | **String** |  |  |
|**customerId** | **String** |  |  |
|**invoice** | **Map&lt;String, Object&gt;** |  |  |
|**totals** | [**InvoiceTotalsOut**](InvoiceTotalsOut.md) |  |  |
|**createdAt** | **String** |  |  |
|**updatedAt** | **String** |  |  |
|**finalizedAt** | **String** |  |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| DRAFT | &quot;draft&quot; |
| FINALIZED | &quot;finalized&quot; |
| SENT | &quot;sent&quot; |
| PAID | &quot;paid&quot; |
| VOID | &quot;void&quot; |
| ARCHIVED | &quot;archived&quot; |



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



