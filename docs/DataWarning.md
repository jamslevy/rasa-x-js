# RasaXHttpApi.DataWarning

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **String** | Entity being warned about * &#x60;data&#x60; - Training data. * &#x60;blankIntent&#x60; - Training data with blank intent values. * &#x60;intent&#x60; - Intents to which your training data are classified. * &#x60;dataPerIntent&#x60; - Training data classified to the intent specified in &#x60;meta&#x60;.  | [optional] 
**min** | **Number** | Either &#x60;min&#x60; or &#x60;max&#x60; will always be present | [optional] 
**max** | **Number** | Either &#x60;min&#x60; or &#x60;max&#x60; will always be present | [optional] 
**count** | **Number** |  | [optional] 
**meta** | [**OneOfstringobject**](OneOfstringobject.md) |  | [optional] 



## Enum: TypeEnum


* `data` (value: `"data"`)

* `blankIntent` (value: `"blankIntent"`)

* `intent` (value: `"intent"`)

* `dataPerIntent` (value: `"dataPerIntent"`)




