# RasaXHttpApi.EvaluationApi

All URIs are relative to *http://api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**predictNextAction**](EvaluationApi.md#predictNextAction) | **POST** /conversations/{conversation_id}/predict | Predicts the next action in the conversation.



## predictNextAction

> PredictResult predictNextAction(conversationId, opts)

Predicts the next action in the conversation.

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.EvaluationApi();
let conversationId = conversation_id; // String | Sender ID
let opts = {
  'includeEvents': "'ALL'" // String | 
};
apiInstance.predictNextAction(conversationId, opts, (error, data, response) => {
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
 **includeEvents** | **String**|  | [optional] [default to &#39;ALL&#39;]

### Return type

[**PredictResult**](PredictResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

