# RasaXHttpApi.TemplateApi

All URIs are relative to *http://api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteTemplate**](TemplateApi.md#deleteTemplate) | **DELETE** /templates/{template_id} | Delete a response template



## deleteTemplate

> String deleteTemplate(templateId)

Delete a response template

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.TemplateApi();
let templateId = 5bb89a7e3b18fb3d95495f2e; // String | Template ID
apiInstance.deleteTemplate(templateId, (error, data, response) => {
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
 **templateId** | **String**| Template ID | 

### Return type

**String**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: text/plain

