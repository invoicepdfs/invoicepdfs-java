

# ReadyResponse


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**dependencies** | [**Map&lt;String, InnerEnum&gt;**](#Map&lt;String, InnerEnum&gt;) |  |  |
|**workers** | **Map&lt;String, String&gt;** |  |  [optional] |
|**degraded** | **List&lt;String&gt;** |  |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| READY | &quot;ready&quot; |
| NOT_READY | &quot;not_ready&quot; |



## Enum: Map&lt;String, InnerEnum&gt;

| Name | Value |
|---- | -----|
| OK | &quot;ok&quot; |
| ERROR | &quot;error&quot; |



