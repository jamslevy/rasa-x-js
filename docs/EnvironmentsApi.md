# RasaXHttpApi.EnvironmentsApi

All URIs are relative to *http://api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getEnvironmentsConfig**](EnvironmentsApi.md#getEnvironmentsConfig) | **GET** /environments | Retrieve Platform deployment environment metadata
[**saveEnvironmentsConfig**](EnvironmentsApi.md#saveEnvironmentsConfig) | **PUT** /environments | Save Platform deployment environment config



## getEnvironmentsConfig

> InlineResponse20010 getEnvironmentsConfig()

Retrieve Platform deployment environment metadata

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.EnvironmentsApi();
apiInstance.getEnvironmentsConfig((error, data, response) => {
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

[**InlineResponse20010**](InlineResponse20010.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## saveEnvironmentsConfig

> InlineResponse20010 saveEnvironmentsConfig(inlineObject10)

Save Platform deployment environment config

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.EnvironmentsApi();
let inlineObject10 = new RasaXHttpApi.InlineObject10(); // InlineObject10 | 
apiInstance.saveEnvironmentsConfig(inlineObject10, (error, data, response) => {
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
 **inlineObject10** | [**InlineObject10**](InlineObject10.md)|  | 

### Return type

[**InlineResponse20010**](InlineResponse20010.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

