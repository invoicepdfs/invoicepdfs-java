

# DocumentOutputOptions


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**format** | [**FormatEnum**](#FormatEnum) |  |  [optional] |
|**delivery** | [**DeliveryEnum**](#DeliveryEnum) |  |  [optional] |
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



