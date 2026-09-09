

# ComplianceRulesetOut

One ruleset the document was held to, and whether it actually ran.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** |  |  |
|**label** | **String** |  |  |
|**version** | **String** | The upstream release of the rules. Empty for checks with no version of their own. |  [optional] |
|**ran** | **Boolean** | False when this ruleset could not be run at all. A ruleset that did not run is not a pass — &#x60;valid&#x60; only reports what was checked. |  |
|**reason** | **String** |  |  [optional] |



