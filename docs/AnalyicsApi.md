# RasaXHttpApi.AnalyicsApi

All URIs are relative to *http://api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getConversationStatistics**](AnalyicsApi.md#getConversationStatistics) | **GET** /statistics | Fetch conversation statistics



## getConversationStatistics

> ConversationStatistics getConversationStatistics()

Fetch conversation statistics

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.AnalyicsApi();
apiInstance.getConversationStatistics((error, data, response) => {
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

[**ConversationStatistics**](ConversationStatistics.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

