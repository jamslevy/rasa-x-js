# RasaXHttpApi.AnalyticsApi

All URIs are relative to *http://api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**userAnalytics**](AnalyticsApi.md#userAnalytics) | **GET** /analytics | Fetch analytics



## userAnalytics

> AnalyticsResult userAnalytics(start, end, window)

Fetch analytics

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.AnalyticsApi();
let start = 2018-01-01T11:03:01.141; // String | Start time. Accepts ISO-8601 format (as in the example) or Unix time.
let end = 2018-11-02T13:44:09.932; // String | End time. Accepts ISO-8601 format (as in the example) or Unix time.
let window = 1d; // String | Bin size used in the accumulation of the requested analytics result. If not specified, 10 bins are returned by default. Multiple formats are supported. A full list is available at https://pypi.org/project/pytimeparse/1.1.8/.
apiInstance.userAnalytics(start, end, window, (error, data, response) => {
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
 **start** | **String**| Start time. Accepts ISO-8601 format (as in the example) or Unix time. | 
 **end** | **String**| End time. Accepts ISO-8601 format (as in the example) or Unix time. | 
 **window** | **String**| Bin size used in the accumulation of the requested analytics result. If not specified, 10 bins are returned by default. Multiple formats are supported. A full list is available at https://pypi.org/project/pytimeparse/1.1.8/. | 

### Return type

[**AnalyticsResult**](AnalyticsResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

