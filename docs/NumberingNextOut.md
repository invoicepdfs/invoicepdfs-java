

# NumberingNextOut

What POST /numbering-sequences/{id}/next allocated.  The number is the point of the call. It used to answer with the sequence row instead, so a caller burned a number and had to reconstruct the string itself from prefix, date pattern and padding — the one thing the endpoint exists to do for them.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**number** | **String** |  |  |
|**sequenceId** | **String** |  |  |
|**nextNumber** | **Integer** | The counter after this allocation |  |



