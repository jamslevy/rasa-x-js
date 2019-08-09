# RasaXHttpApi.ConversationMetadata

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**conversationId** | **String** | Id of this conversation | [optional] 
**latestEventTime** | **Number** | Timestamp of most recent event (in seconds) | [optional] 
**latestInputChannel** | **String** | Name of the input channel last used | [optional] 
**intents** | **[String]** | Set of intents in the conversation | [optional] 
**actions** | **[String]** | Set of actions in the conversation | [optional] 
**minimumActionConfidence** | **Number** | Minimum action confidence in the conversation | [optional] 
**inTrainingData** | **Boolean** | Whether the entire conversation appear in training data | [optional] 
**policies** | **[String]** | Set of policies used in the action predictions | [optional] 
**nUserMessages** | **Number** | Number of user messages in the conversation | [optional] 
**flaggedMessages** | **[Object]** | List of flagged messages | [optional] 
**unflaggedMessages** | **[Object]** | List of unflagged messages | [optional] 


