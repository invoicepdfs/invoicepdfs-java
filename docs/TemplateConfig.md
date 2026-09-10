

# TemplateConfig

What a custom template is: a built-in design plus the brand to render it in.  A custom template is not a design of its own — it names one of the built-ins in ``base_template_id`` and carries the values below, which are the same ones ``data.branding`` carries. They are applied *underneath* a request's own branding, so a document that states a colour still wins and one template can serve several brands.  Typed rather than the free-form object it used to be: nothing read that object, so every key in it was equally correct and a caller could keep sending ``primary_colour`` forever without a word back. Unset here means \"the template has no opinion\" — unlike ``Branding``, whose every field has a non-empty default and so cannot say that.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**primaryColor** | **String** |  |  [optional] |
|**accentColor** | **String** |  |  [optional] |
|**fontFamily** | **String** |  |  [optional] |
|**headerText** | **String** |  |  [optional] |
|**footerText** | **String** |  |  [optional] |



