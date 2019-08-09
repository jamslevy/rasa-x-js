# RasaXHttpApi.ConversationsApi

All URIs are relative to *http://api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**correctMessage**](ConversationsApi.md#correctMessage) | **PUT** /conversations/{conversation_id}/messages/{message_timestamp}/intent | Correct message intent
[**deleteFlagFromConversation**](ConversationsApi.md#deleteFlagFromConversation) | **DELETE** /conversations/{conversation_id}/messages/{message_timestamp}/flag | Removes a flag from a message
[**downloadDebugDumpJson**](ConversationsApi.md#downloadDebugDumpJson) | **GET** /conversations/{conversation_id}/debug-dump.json | Download debug dump in JSON format
[**downloadDebugDumpMarkdown**](ConversationsApi.md#downloadDebugDumpMarkdown) | **GET** /conversations/{conversation_id}/debug-dump.md | Download debug dump in Markdown format
[**flagMessage**](ConversationsApi.md#flagMessage) | **PUT** /conversations/{conversation_id}/messages/{message_timestamp}/flag | Flags this message
[**getConversation**](ConversationsApi.md#getConversation) | **GET** /conversations/{conversation_id} | Fetch tracker for a conversation id
[**getConversations**](ConversationsApi.md#getConversations) | **GET** /conversations | Fetch list of conversations
[**getEvents**](ConversationsApi.md#getEvents) | **GET** /conversations/{conversation_id}/events | Fetch events in conversation with conversation
[**getMessages**](ConversationsApi.md#getMessages) | **GET** /conversations/{conversation_id}/messages | Fetch messages in conversation
[**getUniqueActions**](ConversationsApi.md#getUniqueActions) | **GET** /conversationActions | Fetch a list of unique actions from all conversations
[**getUniqueEntities**](ConversationsApi.md#getUniqueEntities) | **GET** /conversationEntities | Fetch a list of unique entities from all conversations
[**getUniqueIntents**](ConversationsApi.md#getUniqueIntents) | **GET** /conversationIntents | Fetch a list of unique intents from all conversations
[**getUniquePolicies**](ConversationsApi.md#getUniquePolicies) | **GET** /conversationPolicies | Fetch a list of unique Rasa Core policies in all conversations
[**putChat**](ConversationsApi.md#putChat) | **POST** /chat | Endpoint to have a conversation with the assistant
[**removeMessageCorrection**](ConversationsApi.md#removeMessageCorrection) | **DELETE** /conversations/{conversation_id}/messages/{message_timestamp}/intent | Undoes the correction of message
[**sendMessage**](ConversationsApi.md#sendMessage) | **POST** /conversations/{conversation_id}/messages | Post a message to a conversation



## correctMessage

> correctMessage(conversationId, messageTimestamp, projectId, inlineObject4, opts)

Correct message intent

Corrects the intent of the message and possible adds it to the training data

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.ConversationsApi();
let conversationId = conversation_id; // String | Sender ID
let messageTimestamp = 3.4; // Number | 
let projectId = default; // String | Project ID
let inlineObject4 = new RasaXHttpApi.InlineObject4(); // InlineObject4 | 
let opts = {
  'environment': "environment_example" // String | Deployment environment to be used in query
};
apiInstance.correctMessage(conversationId, messageTimestamp, projectId, inlineObject4, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **conversationId** | **String**| Sender ID | 
 **messageTimestamp** | **Number**|  | 
 **projectId** | **String**| Project ID | 
 **inlineObject4** | [**InlineObject4**](InlineObject4.md)|  | 
 **environment** | **String**| Deployment environment to be used in query | [optional] 

### Return type

null (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## deleteFlagFromConversation

> deleteFlagFromConversation(conversationId, messageTimestamp)

Removes a flag from a message

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.ConversationsApi();
let conversationId = conversation_id; // String | Sender ID
let messageTimestamp = 3.4; // Number | 
apiInstance.deleteFlagFromConversation(conversationId, messageTimestamp, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **conversationId** | **String**| Sender ID | 
 **messageTimestamp** | **Number**|  | 

### Return type

null (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## downloadDebugDumpJson

> Object downloadDebugDumpJson(conversationId, opts)

Download debug dump in JSON format

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.ConversationsApi();
let conversationId = conversation_id; // String | Sender ID
let opts = {
  'until': 56, // Number | Upper bound of timestamp for data to be dumped
  'useHistory': true // Boolean | Whether to include data before the last reset
};
apiInstance.downloadDebugDumpJson(conversationId, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **conversationId** | **String**| Sender ID | 
 **until** | **Number**| Upper bound of timestamp for data to be dumped | [optional] 
 **useHistory** | **Boolean**| Whether to include data before the last reset | [optional] 

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## downloadDebugDumpMarkdown

> Object downloadDebugDumpMarkdown(conversationId, opts)

Download debug dump in Markdown format

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.ConversationsApi();
let conversationId = conversation_id; // String | Sender ID
let opts = {
  'until': 56, // Number | Upper bound of timestamp for data to be dumped
  'useHistory': true // Boolean | Whether to include data before the last reset
};
apiInstance.downloadDebugDumpMarkdown(conversationId, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **conversationId** | **String**| Sender ID | 
 **until** | **Number**| Upper bound of timestamp for data to be dumped | [optional] 
 **useHistory** | **Boolean**| Whether to include data before the last reset | [optional] 

### Return type

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## flagMessage

> flagMessage(conversationId, messageTimestamp)

Flags this message

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.ConversationsApi();
let conversationId = conversation_id; // String | Sender ID
let messageTimestamp = 3.4; // Number | 
apiInstance.flagMessage(conversationId, messageTimestamp, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **conversationId** | **String**| Sender ID | 
 **messageTimestamp** | **Number**|  | 

### Return type

null (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## getConversation

> [Conversation] getConversation(conversationId, opts)

Fetch tracker for a conversation id

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.ConversationsApi();
let conversationId = conversation_id; // String | Sender ID
let opts = {
  'environment': "environment_example" // String | Deployment environment to be used in query
};
apiInstance.getConversation(conversationId, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **conversationId** | **String**| Sender ID | 
 **environment** | **String**| Deployment environment to be used in query | [optional] 

### Return type

[**[Conversation]**](Conversation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getConversations

> [ConversationMetadata] getConversations(opts)

Fetch list of conversations

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.ConversationsApi();
let opts = {
  'environment': "environment_example", // String | Deployment environment to be used in query
  'intent': "'null'", // String | Comma-separated intents to filter on
  'entity': "'null'", // String | Comma-separated entities to filter on
  'action': "'null'", // String | Comma-separated actions to filter on
  'text': "'null'", // String | User utterance text to filter on
  'start': 3.4, // Number | Minimum timestamp of latest user event
  'until': 3.4, // Number | Maximum timestamp of latest user event
  'policies': "'null'", // String | Comma-separated list of policies used for prediction
  'maximumConfidence': 3.4, // Number | Maximum value of the minimum action confidence
  'minimumUserMessages': 3.4, // Number | Minimum number of user messages per conversation
  'inTrainingData': true, // Boolean | Only show conversations that appear in the training data. If false, only show conversations not appearing in training data . If unset, show all conversations.
  'sortByConfidence': true, // Boolean | Sort conversations that are not found in the training data by their minimum action confidence from high to low. Has no effect if `in_training_data` is anything other than false.
  'sortByLatestEventTime': true, // Boolean | Sort conversations by their latest activity from most recent to least recent.
  'isFlagged': false, // Boolean | Filter for conversations which contain flagged messages.
  'excludeSelf': false // Boolean | Exclude currently authenticated user from conversations.
};
apiInstance.getConversations(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **environment** | **String**| Deployment environment to be used in query | [optional] 
 **intent** | **String**| Comma-separated intents to filter on | [optional] [default to &#39;null&#39;]
 **entity** | **String**| Comma-separated entities to filter on | [optional] [default to &#39;null&#39;]
 **action** | **String**| Comma-separated actions to filter on | [optional] [default to &#39;null&#39;]
 **text** | **String**| User utterance text to filter on | [optional] [default to &#39;null&#39;]
 **start** | **Number**| Minimum timestamp of latest user event | [optional] 
 **until** | **Number**| Maximum timestamp of latest user event | [optional] 
 **policies** | **String**| Comma-separated list of policies used for prediction | [optional] [default to &#39;null&#39;]
 **maximumConfidence** | **Number**| Maximum value of the minimum action confidence | [optional] 
 **minimumUserMessages** | **Number**| Minimum number of user messages per conversation | [optional] 
 **inTrainingData** | **Boolean**| Only show conversations that appear in the training data. If false, only show conversations not appearing in training data . If unset, show all conversations. | [optional] 
 **sortByConfidence** | **Boolean**| Sort conversations that are not found in the training data by their minimum action confidence from high to low. Has no effect if &#x60;in_training_data&#x60; is anything other than false. | [optional] [default to true]
 **sortByLatestEventTime** | **Boolean**| Sort conversations by their latest activity from most recent to least recent. | [optional] [default to true]
 **isFlagged** | **Boolean**| Filter for conversations which contain flagged messages. | [optional] [default to false]
 **excludeSelf** | **Boolean**| Exclude currently authenticated user from conversations. | [optional] [default to false]

### Return type

[**[ConversationMetadata]**](ConversationMetadata.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getEvents

> [Event] getEvents(conversationId, opts)

Fetch events in conversation with conversation

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.ConversationsApi();
let conversationId = conversation_id; // String | Sender ID
let opts = {
  'environment': "environment_example", // String | Deployment environment to be used in query
  'until': 56, // Number | Upper bound of timestamp for data to be dumped
  'useHistory': true // Boolean | Whether to include data before the last reset
};
apiInstance.getEvents(conversationId, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **conversationId** | **String**| Sender ID | 
 **environment** | **String**| Deployment environment to be used in query | [optional] 
 **until** | **Number**| Upper bound of timestamp for data to be dumped | [optional] 
 **useHistory** | **Boolean**| Whether to include data before the last reset | [optional] 

### Return type

[**[Event]**](Event.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getMessages

> [Event] getMessages(conversationId, opts)

Fetch messages in conversation

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.ConversationsApi();
let conversationId = conversation_id; // String | Sender ID
let opts = {
  'environment': "environment_example", // String | Deployment environment to be used in query
  'until': 56, // Number | Upper bound of timestamp for data to be dumped
  'useHistory': true // Boolean | Whether to include data before the last reset
};
apiInstance.getMessages(conversationId, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **conversationId** | **String**| Sender ID | 
 **environment** | **String**| Deployment environment to be used in query | [optional] 
 **until** | **Number**| Upper bound of timestamp for data to be dumped | [optional] 
 **useHistory** | **Boolean**| Whether to include data before the last reset | [optional] 

### Return type

[**[Event]**](Event.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getUniqueActions

> [String] getUniqueActions()

Fetch a list of unique actions from all conversations

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.ConversationsApi();
apiInstance.getUniqueActions((error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

This endpoint does not need any parameter.

### Return type

**[String]**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getUniqueEntities

> [String] getUniqueEntities()

Fetch a list of unique entities from all conversations

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.ConversationsApi();
apiInstance.getUniqueEntities((error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

This endpoint does not need any parameter.

### Return type

**[String]**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getUniqueIntents

> [String] getUniqueIntents()

Fetch a list of unique intents from all conversations

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.ConversationsApi();
apiInstance.getUniqueIntents((error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

This endpoint does not need any parameter.

### Return type

**[String]**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getUniquePolicies

> [String] getUniquePolicies()

Fetch a list of unique Rasa Core policies in all conversations

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.ConversationsApi();
apiInstance.getUniquePolicies((error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

This endpoint does not need any parameter.

### Return type

**[String]**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## putChat

> [Object] putChat(inlineObject9)

Endpoint to have a conversation with the assistant

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.ConversationsApi();
let inlineObject9 = new RasaXHttpApi.InlineObject9(); // InlineObject9 | 
apiInstance.putChat(inlineObject9, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inlineObject9** | [**InlineObject9**](InlineObject9.md)|  | 

### Return type

**[Object]**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## removeMessageCorrection

> removeMessageCorrection(conversationId, messageTimestamp, projectId)

Undoes the correction of message

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.ConversationsApi();
let conversationId = conversation_id; // String | Sender ID
let messageTimestamp = 3.4; // Number | 
let projectId = default; // String | Project ID
apiInstance.removeMessageCorrection(conversationId, messageTimestamp, projectId, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **conversationId** | **String**| Sender ID | 
 **messageTimestamp** | **Number**|  | 
 **projectId** | **String**| Project ID | 

### Return type

null (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## sendMessage

> [Object] sendMessage(conversationId, message, opts)

Post a message to a conversation

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.ConversationsApi();
let conversationId = conversation_id; // String | Sender ID
let message = new RasaXHttpApi.Message(); // Message | 
let opts = {
  'environment': "environment_example" // String | Deployment environment to be used in query
};
apiInstance.sendMessage(conversationId, message, opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **conversationId** | **String**| Sender ID | 
 **message** | [**Message**](Message.md)|  | 
 **environment** | **String**| Deployment environment to be used in query | [optional] 

### Return type

**[Object]**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

