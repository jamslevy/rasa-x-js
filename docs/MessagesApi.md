# RasaXHttpApi.MessagesApi

All URIs are relative to *http://api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createEvent**](MessagesApi.md#createEvent) | **POST** /conversations/{conversation_id}/events | Create a new event in the tracker of a conversation
[**getSuggestions**](MessagesApi.md#getSuggestions) | **GET** /projects/{project_id}/logs | Get suggestions
[**parseText**](MessagesApi.md#parseText) | **POST** /projects/{project_id}/logs | Parse text and create a new log entry
[**runAction**](MessagesApi.md#runAction) | **POST** /conversations/{conversation_id}/execute | Run an action in a conversation.
[**updateEvent**](MessagesApi.md#updateEvent) | **PUT** /conversations/{conversation_id}/events | Update events in the tracker of a conversation



## createEvent

> Event createEvent(conversationId, event)

Create a new event in the tracker of a conversation

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.MessagesApi();
let conversationId = conversation_id; // String | Sender ID
let event = new RasaXHttpApi.Event(); // Event | 
apiInstance.createEvent(conversationId, event, (error, data, response) => {
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
 **event** | [**Event**](Event.md)|  | 

### Return type

[**Event**](Event.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## getSuggestions

> [Suggestion] getSuggestions(projectId, opts)

Get suggestions

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.MessagesApi();
let projectId = default; // String | Project ID
let opts = {
  'q': "q_example", // String | Query string
  'intent': "'null'", // String | Comma-separated intents to filter on
  'limit': 56, // Number | 
  'offset': 0 // Number | 
};
apiInstance.getSuggestions(projectId, opts, (error, data, response) => {
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
 **projectId** | **String**| Project ID | 
 **q** | **String**| Query string | [optional] 
 **intent** | **String**| Comma-separated intents to filter on | [optional] [default to &#39;null&#39;]
 **limit** | **Number**|  | [optional] 
 **offset** | **Number**|  | [optional] [default to 0]

### Return type

[**[Suggestion]**](Suggestion.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## parseText

> Suggestion parseText(projectId, opts)

Parse text and create a new log entry

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.MessagesApi();
let projectId = default; // String | Project ID
let opts = {
  'q': "q_example" // String | Query string
};
apiInstance.parseText(projectId, opts, (error, data, response) => {
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
 **projectId** | **String**| Project ID | 
 **q** | **String**| Query string | [optional] 

### Return type

[**Suggestion**](Suggestion.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## runAction

> InlineResponse2004 runAction(conversationId, inlineObject5, opts)

Run an action in a conversation.

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.MessagesApi();
let conversationId = conversation_id; // String | Sender ID
let inlineObject5 = new RasaXHttpApi.InlineObject5(); // InlineObject5 | 
let opts = {
  'includeEvents': "'ALL'" // String | 
};
apiInstance.runAction(conversationId, inlineObject5, opts, (error, data, response) => {
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
 **inlineObject5** | [**InlineObject5**](InlineObject5.md)|  | 
 **includeEvents** | **String**|  | [optional] [default to &#39;ALL&#39;]

### Return type

[**InlineResponse2004**](InlineResponse2004.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## updateEvent

> [Event] updateEvent(conversationId, event)

Update events in the tracker of a conversation

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.MessagesApi();
let conversationId = conversation_id; // String | Sender ID
let event = [new RasaXHttpApi.Event()]; // [Event] | 
apiInstance.updateEvent(conversationId, event, (error, data, response) => {
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
 **event** | [**[Event]**](Event.md)|  | 

### Return type

[**[Event]**](Event.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

