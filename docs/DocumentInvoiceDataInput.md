

# DocumentInvoiceDataInput


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**invoiceNumber** | **String** |  |  |
|**issueDate** | **LocalDate** |  |  |
|**dueDate** | **LocalDate** |  |  [optional] |
|**currency** | **String** |  |  |
|**seller** | [**DocumentPartyInput**](DocumentPartyInput.md) |  |  |
|**buyer** | [**DocumentPartyInput**](DocumentPartyInput.md) |  |  |
|**shipTo** | [**DocumentPartyInput**](DocumentPartyInput.md) |  |  [optional] |
|**lineItems** | [**List&lt;DocumentLineItemInput&gt;**](DocumentLineItemInput.md) |  |  |
|**discounts** | [**List&lt;DocumentDiscountInput&gt;**](DocumentDiscountInput.md) |  |  [optional] |
|**shipping** | [**DocumentShippingInput**](DocumentShippingInput.md) |  |  [optional] |
|**customFields** | [**List&lt;DocumentCustomFieldInput&gt;**](DocumentCustomFieldInput.md) |  |  [optional] |
|**payment** | [**DocumentPaymentInput**](DocumentPaymentInput.md) |  |  [optional] |
|**branding** | [**DocumentBrandingInput**](DocumentBrandingInput.md) |  |  [optional] |



