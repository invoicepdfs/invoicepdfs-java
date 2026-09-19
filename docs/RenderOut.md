

# RenderOut


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** |  |  |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**documentType** | [**DocumentTypeEnum**](#DocumentTypeEnum) |  |  |
|**templateId** | **String** |  |  |
|**templateVersion** | **Integer** |  |  [optional] |
|**format** | [**FormatEnum**](#FormatEnum) |  |  |
|**downloadUrl** | **String** |  |  [optional] |
|**expiresAt** | **String** |  |  [optional] |
|**calculation** | [**CalculationBreakdown**](CalculationBreakdown.md) |  |  |
|**createdAt** | **String** |  |  |
|**compliance** | [**RenderComplianceOut**](RenderComplianceOut.md) |  |  [optional] |
|**failure** | [**RenderFailureOut**](RenderFailureOut.md) |  |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| QUEUED | &quot;queued&quot; |
| PROCESSING | &quot;processing&quot; |
| COMPLETED | &quot;completed&quot; |
| FAILED | &quot;failed&quot; |



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



## Enum: FormatEnum

| Name | Value |
|---- | -----|
| PDF | &quot;pdf&quot; |



