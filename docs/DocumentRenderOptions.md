

# DocumentRenderOptions

Render options for a document that is already stored.  For ``POST /documents/{id}/renders``. The stateless ``POST /documents/render`` takes the whole document inline instead.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**templateId** | **String** |  |  [optional] |
|**templateVersion** | **Integer** |  |  [optional] |
|**pageSize** | **String** |  |  [optional] |
|**expiresIn** | **Integer** | How long the render stays downloadable, in seconds (1 minute to 7 days). It is also the lifetime of the signature in &#x60;download_url&#x60;, which is why it is bounded: an unbounded value meant an unbounded grant. A value below the floor used to be accepted and produced a render that had already expired. |  [optional] |
|**format** | [**FormatEnum**](#FormatEnum) | &#x60;facturx_pdf&#x60; embeds the EN 16931 CII XML in a PDF/A-3, which is what a French or German counterparty means by Factur-X or ZUGFeRD. |  [optional] |



## Enum: FormatEnum

| Name | Value |
|---- | -----|
| PDF | &quot;pdf&quot; |
| FACTURX_PDF | &quot;facturx_pdf&quot; |



