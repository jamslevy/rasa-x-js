# RasaXHttpApi.IntentsApi

All URIs are relative to *http://api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getIntents**](IntentsApi.md#getIntents) | **GET** /projects/{project_id}/intents | List intents



## getIntents

> [IntentInformation] getIntents(projectId, opts)

List intents

Intents used in training examples, domain, or temporary intents

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.IntentsApi();
let projectId = default; // String | Project ID
let opts = {
  'temporary': true // Boolean | If `True` the query will also include temporary intents
};
apiInstance.getIntents(projectId, opts, (error, data, response) => {
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
 **temporary** | **Boolean**| If &#x60;True&#x60; the query will also include temporary intents | [optional] 

### Return type

[**[IntentInformation]**](IntentInformation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

