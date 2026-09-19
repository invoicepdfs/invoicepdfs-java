

# RenderFailureOut

Why a render failed, in the same shape the synchronous path returns.  A synchronous render of a document EN 16931 would reject answers `422 compliance_failed` with every violation at once — a list of fields to go and fill in. A queued render has to be able to say the same thing: the caller who chose `async` did not choose a worse answer.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**code** | **String** | &#x60;compliance_failed&#x60; for a document that is well-formed and would be rejected by the ruleset it asked for; &#x60;unprocessable_entity&#x60; for one the renderer could not make sense of. The same codes the synchronous path returns. |  |
|**message** | **String** |  |  |
|**details** | **Map&lt;String, Object&gt;** |  |  [optional] |



