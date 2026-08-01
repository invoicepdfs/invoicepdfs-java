

# BatchOut


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** |  |  |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**operation** | **String** |  |  |
|**templateId** | **String** |  |  |
|**totalItems** | **Integer** |  |  |
|**completedItems** | **Integer** |  |  |
|**failedItems** | **Integer** |  |  |
|**createdAt** | **String** |  |  |
|**updatedAt** | **String** |  |  |
|**completedAt** | **String** |  |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| QUEUED | &quot;queued&quot; |
| PROCESSING | &quot;processing&quot; |
| COMPLETED | &quot;completed&quot; |
| FAILED | &quot;failed&quot; |
| CANCELLED | &quot;cancelled&quot; |



