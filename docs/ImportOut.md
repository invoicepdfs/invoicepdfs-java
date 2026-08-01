

# ImportOut


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** |  |  |
|**sourceFormat** | **String** |  |  |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**totalRows** | **Integer** |  |  |
|**importedRows** | **Integer** |  |  |
|**failedRows** | **Integer** |  |  |
|**errors** | **List&lt;Map&lt;String, Object&gt;&gt;** |  |  [optional] |
|**createdAt** | **String** |  |  |
|**updatedAt** | **String** |  |  |
|**completedAt** | **String** |  |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| PENDING | &quot;pending&quot; |
| PROCESSING | &quot;processing&quot; |
| COMPLETED | &quot;completed&quot; |
| FAILED | &quot;failed&quot; |
| CANCELLED | &quot;cancelled&quot; |



