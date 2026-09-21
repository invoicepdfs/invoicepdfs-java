

# WebhookEndpointCreatedOut

A newly created endpoint, including its signing secret.  The only time the secret is returned. Store it now: reading or listing endpoints never includes it, and the only way to obtain another is to rotate, which invalidates this one.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** |  |  |
|**url** | **String** |  |  |
|**description** | **String** |  |  [optional] |
|**events** | **List&lt;String&gt;** |  |  |
|**isActive** | **Boolean** |  |  |
|**createdAt** | **String** |  |  |
|**updatedAt** | **String** |  |  |
|**secret** | **String** |  |  |



