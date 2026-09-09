

# ComplianceCheckOut


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**profile** | **String** |  |  |
|**rulesetVersion** | **String** | The version these rules came from. Worth recording alongside any document you file — rulesets revise, and &#39;which rules did this pass?&#39; is what an audit asks years later. &#x60;rulesets&#x60; breaks the same answer down per ruleset. |  |
|**valid** | **Boolean** | Nothing fatal was found. Read it with &#x60;fully_checked&#x60; — on its own it says what was checked came back clean, not that everything was checked. |  |
|**fullyChecked** | **Boolean** | Every ruleset that applies to this profile ran. False means at least one could not, and &#x60;rulesets&#x60; says which and why. |  [optional] |
|**rulesets** | [**List&lt;ComplianceRulesetOut&gt;**](ComplianceRulesetOut.md) | Every ruleset the document was held to, including the mandatory-field check, at the version that ran. |  [optional] |
|**violations** | [**List&lt;ComplianceViolationOut&gt;**](ComplianceViolationOut.md) | Every violation found, not the first — fixing one field per round trip is the experience this avoids. Ordered mandatory-field findings first, since those name a field you can go and change. |  [optional] |



