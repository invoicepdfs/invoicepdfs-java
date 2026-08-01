

# NumberingSequenceCreateRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** |  |  |
|**documentType** | [**DocumentTypeEnum**](#DocumentTypeEnum) |  |  [optional] |
|**prefix** | **String** |  |  [optional] |
|**datePattern** | **String** |  |  [optional] |
|**padding** | **Integer** |  |  [optional] |
|**nextNumber** | **Integer** |  |  [optional] |
|**reset** | [**ResetEnum**](#ResetEnum) |  |  [optional] |



## Enum: DocumentTypeEnum

| Name | Value |
|---- | -----|
| INVOICE | &quot;invoice&quot; |
| CREDIT_NOTE | &quot;credit_note&quot; |



## Enum: ResetEnum

| Name | Value |
|---- | -----|
| NEVER | &quot;never&quot; |
| YEARLY | &quot;yearly&quot; |
| MONTHLY | &quot;monthly&quot; |



