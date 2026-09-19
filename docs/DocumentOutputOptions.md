

# DocumentOutputOptions


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**format** | [**FormatEnum**](#FormatEnum) |  |  [optional] |
|**delivery** | [**DeliveryEnum**](#DeliveryEnum) |  |  [optional] |
|**mode** | [**ModeEnum**](#ModeEnum) | &#x60;sync&#x60; renders inside the request and answers with the finished document. &#x60;async&#x60; returns &#x60;202&#x60; with a &#x60;queued&#x60; render a worker picks up; follow it with &#x60;GET /renders/{id}&#x60;. Use it for bursts — rendering is CPU-bound, so a hundred at once queue behind each other whichever mode you ask for, and only one of the two holds a connection open while they do. |  [optional] |
|**expiresIn** | **Integer** | How long the render stays downloadable, in seconds (1 minute to 7 days). It is also the lifetime of the signature in &#x60;download_url&#x60;, which is why it is bounded: an unbounded value meant an unbounded grant. A value below the floor used to be accepted and produced a render that had already expired. |  [optional] |



## Enum: FormatEnum

| Name | Value |
|---- | -----|
| PDF | &quot;pdf&quot; |
| FACTURX_PDF | &quot;facturx_pdf&quot; |



## Enum: DeliveryEnum

| Name | Value |
|---- | -----|
| URL | &quot;url&quot; |
| BINARY | &quot;binary&quot; |



## Enum: ModeEnum

| Name | Value |
|---- | -----|
| SYNC | &quot;sync&quot; |
| ASYNC | &quot;async&quot; |



