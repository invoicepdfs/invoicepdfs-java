

# CreditNoteOut


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** |  |  |
|**invoiceId** | **String** |  |  |
|**creditNoteNumber** | **String** |  |  |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**reason** | **String** |  |  [optional] |
|**currency** | **String** |  |  |
|**totals** | [**InvoiceTotalsOut**](InvoiceTotalsOut.md) |  |  |
|**issueDate** | **LocalDate** |  |  |
|**createdAt** | **String** |  |  |
|**updatedAt** | **String** |  |  |
|**finalizedAt** | **String** |  |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| DRAFT | &quot;draft&quot; |
| FINALIZED | &quot;finalized&quot; |



