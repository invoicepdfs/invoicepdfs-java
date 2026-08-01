

# RecurringInvoiceCreateRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**businessProfileId** | **String** |  |  |
|**customerId** | **String** |  |  |
|**frequency** | **String** | daily, weekly, monthly, quarterly, or yearly |  |
|**interval** | **Integer** | Every N periods |  [optional] |
|**startDate** | **LocalDate** | Date of the first invoice |  |
|**endDate** | **LocalDate** |  |  [optional] |
|**maxOccurrences** | **Integer** |  |  [optional] |
|**numberingSequenceId** | **String** |  |  [optional] |
|**autoFinalize** | **Boolean** | Automatically finalize generated invoices |  [optional] |
|**invoiceTemplate** | [**InvoiceDraftRequest**](InvoiceDraftRequest.md) |  |  |



