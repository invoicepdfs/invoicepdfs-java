

# WebhookDeliveryOut


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** |  |  |
|**endpointId** | **String** |  |  |
|**eventId** | **String** |  |  |
|**eventType** | **String** |  |  |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**httpStatus** | **Integer** |  |  [optional] |
|**attempts** | **Integer** |  |  |
|**errorMessage** | **String** |  |  [optional] |
|**createdAt** | **String** |  |  |
|**deliveredAt** | **String** |  |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| PENDING | &quot;pending&quot; |
| DELIVERED | &quot;delivered&quot; |
| FAILED | &quot;failed&quot; |



