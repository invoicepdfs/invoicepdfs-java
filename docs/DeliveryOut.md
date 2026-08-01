

# DeliveryOut


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** |  |  |
|**invoiceId** | **String** |  |  |
|**to** | **List&lt;String&gt;** |  |  |
|**cc** | **List&lt;String&gt;** |  |  |
|**bcc** | **List&lt;String&gt;** |  |  |
|**subject** | **String** |  |  |
|**message** | **String** |  |  [optional] |
|**attachPdf** | **Boolean** |  |  |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**createdAt** | **String** |  |  |
|**sentAt** | **String** |  |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| QUEUED | &quot;queued&quot; |
| SENT | &quot;sent&quot; |
| DELIVERED | &quot;delivered&quot; |
| BOUNCED | &quot;bounced&quot; |
| FAILED | &quot;failed&quot; |



