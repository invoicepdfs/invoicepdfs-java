

# DocumentRenderOptions

Render options for an already-stored document (``POST /documents/{id}/renders``).  Distinct from ``app.schemas.v1.DocumentRenderRequest``, which carries a full inline document for the stateless ``POST /documents/render``. Two classes sharing one name made FastAPI fall back to module-qualified schema names in the spec (``app__documents__schemas__DocumentRenderRequest``), which the SDK generators turned into ``AppDocumentsSchemasDocumentRenderRequest``.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**templateId** | **String** |  |  [optional] |
|**pageSize** | **String** |  |  [optional] |
|**expiresIn** | **Integer** |  |  [optional] |



