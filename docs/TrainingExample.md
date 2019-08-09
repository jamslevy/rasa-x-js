# RasaXHttpApi.TrainingExample

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | [optional] 
**text** | **String** |  | [optional] 
**intent** | **String** |  | [optional] 
**entities** | [**[TrainingExampleEntities]**](TrainingExampleEntities.md) |  | [optional] 
**hash** | **String** |  | [optional] 
**intentMappedTo** | **String** | Name of the intent which the intent is mapped to. If the intent is a temporary one, it has to be mapped to an existing one to be part of the training. If its value is &#x60;null&#x60; it deletes existing mappings. | [optional] 


