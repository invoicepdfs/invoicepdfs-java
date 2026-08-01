

# InvoiceDraftRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**invoiceNumber** | **String** |  |  |
|**documentType** | [**DocumentTypeEnum**](#DocumentTypeEnum) |  |  [optional] |
|**issueDate** | **LocalDate** |  |  |
|**dueDate** | **LocalDate** |  |  [optional] |
|**currency** | **String** |  |  |
|**locale** | **String** |  |  [optional] |
|**businessProfileId** | **String** |  |  |
|**customerId** | **String** |  |  |
|**shipTo** | [**PostalAddress**](PostalAddress.md) |  |  [optional] |
|**lineItems** | [**List&lt;InvoiceLineItemInput&gt;**](InvoiceLineItemInput.md) |  |  |
|**discounts** | [**List&lt;InvoiceDiscountInput&gt;**](InvoiceDiscountInput.md) |  |  [optional] |
|**shipping** | [**InvoiceShippingInput**](InvoiceShippingInput.md) |  |  [optional] |
|**notes** | [**List&lt;InvoiceNoteInput&gt;**](InvoiceNoteInput.md) |  |  [optional] |
|**terms** | [**List&lt;InvoiceTermInput&gt;**](InvoiceTermInput.md) |  |  [optional] |
|**customFields** | [**List&lt;InvoiceCustomFieldInput&gt;**](InvoiceCustomFieldInput.md) |  |  [optional] |
|**payment** | [**InvoicePaymentInput**](InvoicePaymentInput.md) |  |  [optional] |
|**branding** | [**InvoiceBrandingInput**](InvoiceBrandingInput.md) |  |  [optional] |



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



