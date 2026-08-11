

# ApiErrorResponseError


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**status** | **Integer** | HTTP status, mirroring the response status line. |  |
|**code** | **String** |  |  |
|**message** | **String** |  |  |
|**requestId** | **String** | Trace id for this request; also returned as X-Trace-Id. |  [optional] |
|**details** | **Object** | Error-specific context. Validation failures carry &#x60;fields&#x60;. |  [optional] |



