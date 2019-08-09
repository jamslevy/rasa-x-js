# RasaXHttpApi.ChatTokenApi

All URIs are relative to *http://api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getChatToken**](ChatTokenApi.md#getChatToken) | **GET** /chatToken | Get chat_token, bot_name and description
[**updateChatToken**](ChatTokenApi.md#updateChatToken) | **PUT** /chatToken | Update a bot&#39;s name and description for token



## getChatToken

> ChatToken getChatToken(accessToken)

Get chat_token, bot_name and description

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.ChatTokenApi();
let accessToken = "accessToken_example"; // String | A user's jwt token
apiInstance.getChatToken(accessToken, (error, data, response) => {
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
 **accessToken** | **String**| A user&#39;s jwt token | 

### Return type

[**ChatToken**](ChatToken.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## updateChatToken

> ChatToken updateChatToken(chatToken)

Update a bot&#39;s name and description for token

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.ChatTokenApi();
let chatToken = new RasaXHttpApi.ChatToken(); // ChatToken | 
apiInstance.updateChatToken(chatToken, (error, data, response) => {
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
 **chatToken** | [**ChatToken**](ChatToken.md)|  | 

### Return type

[**ChatToken**](ChatToken.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

