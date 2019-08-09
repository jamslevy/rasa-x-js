# RasaXHttpApi.FeatureFlagsApi

All URIs are relative to *http://api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getFeatureFlags**](FeatureFlagsApi.md#getFeatureFlags) | **GET** /features | Retrieve all features flags
[**updateFeatureFlag**](FeatureFlagsApi.md#updateFeatureFlag) | **POST** /features | Update or create a feature flag



## getFeatureFlags

> [FeatureFlag] getFeatureFlags()

Retrieve all features flags

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.FeatureFlagsApi();
apiInstance.getFeatureFlags((error, data, response) => {
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

[**[FeatureFlag]**](FeatureFlag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## updateFeatureFlag

> FeatureFlag updateFeatureFlag(featureFlag)

Update or create a feature flag

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.FeatureFlagsApi();
let featureFlag = new RasaXHttpApi.FeatureFlag(); // FeatureFlag | 
apiInstance.updateFeatureFlag(featureFlag, (error, data, response) => {
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
 **featureFlag** | [**FeatureFlag**](FeatureFlag.md)|  | 

### Return type

[**FeatureFlag**](FeatureFlag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

