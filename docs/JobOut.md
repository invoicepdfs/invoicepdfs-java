

# JobOut


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** |  |  |
|**type** | **String** |  |  |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**progress** | [**JobProgressOut**](JobProgressOut.md) |  |  |
|**result** | **Map&lt;String, Object&gt;** |  |  [optional] |
|**error** | **String** |  |  [optional] |
|**createdAt** | **String** |  |  |
|**startedAt** | **String** |  |  [optional] |
|**completedAt** | **String** |  |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| QUEUED | &quot;queued&quot; |
| PROCESSING | &quot;processing&quot; |
| COMPLETED | &quot;completed&quot; |
| FAILED | &quot;failed&quot; |
| CANCELLED | &quot;cancelled&quot; |



