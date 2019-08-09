# RasaXHttpApi.LogsApi

All URIs are relative to *http://api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**archiveLog**](LogsApi.md#archiveLog) | **DELETE** /projects/{project_id}/logs/{log_id} | Archive log
[**getLogByHash**](LogsApi.md#getLogByHash) | **GET** /projects/{project_id}/logs/{hash} | Fetch log by its hash
[**getLogs**](LogsApi.md#getLogs) | **GET** /logs | Get the logs of the Rasa X service



## archiveLog

> String archiveLog(projectId, logId)

Archive log

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.LogsApi();
let projectId = default; // String | Project ID
let logId = "logId_example"; // String | 
apiInstance.archiveLog(projectId, logId, (error, data, response) => {
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
 **logId** | **String**|  | 

### Return type

**String**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: text/plain


## getLogByHash

> Suggestion getLogByHash(projectId, hash)

Fetch log by its hash

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.LogsApi();
let projectId = default; // String | Project ID
let hash = b10a8db164e0754105b7a99be72e3fe5; // String | MD5 hash of an NLU example's text field
apiInstance.getLogByHash(projectId, hash, (error, data, response) => {
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
 **hash** | **String**| MD5 hash of an NLU example&#39;s text field | 

### Return type

[**Suggestion**](Suggestion.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getLogs

> getLogs(opts)

Get the logs of the Rasa X service

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.LogsApi();
let opts = {
  'apiToken': "apiToken_example" // String | A user's api token
};
apiInstance.getLogs(opts, (error, data, response) => {
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
 **apiToken** | **String**| A user&#39;s api token | [optional] 

### Return type

null (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/zip, text/plain

