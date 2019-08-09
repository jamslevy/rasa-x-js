# RasaXHttpApi.ProjectApi

All URIs are relative to *http://api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**postProject**](ProjectApi.md#postProject) | **POST** /projects/{project_id} | Create a project



## postProject

> Project postProject(projectId)

Create a project

Not recommended to be used. The frontend only supports a single project.

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.ProjectApi();
let projectId = "projectId_example"; // String | 
apiInstance.postProject(projectId, (error, data, response) => {
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
 **projectId** | **String**|  | 

### Return type

[**Project**](Project.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

