# RasaXHttpApi.TemplatesApi

All URIs are relative to *http://api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getTemplates**](TemplatesApi.md#getTemplates) | **GET** /templates | Get bot response templates
[**modifyTemplate**](TemplatesApi.md#modifyTemplate) | **PUT** /templates/{template_id} | Modify response template
[**postTemplate**](TemplatesApi.md#postTemplate) | **POST** /templates | Add to templates collection



## getTemplates

> InlineResponse2009 getTemplates(opts)

Get bot response templates

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.TemplatesApi();
let opts = {
  'q': "q_example", // String | Template text search string
  'template': "template_example", // String | Templates to filter on (comma-separated)
  'limit': 3.4, // Number | Limit number of responses to return
  'offset': 0 // Number | Offset to consider in window of responses returned
};
apiInstance.getTemplates(opts, (error, data, response) => {
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
 **q** | **String**| Template text search string | [optional] 
 **template** | **String**| Templates to filter on (comma-separated) | [optional] 
 **limit** | **Number**| Limit number of responses to return | [optional] 
 **offset** | **Number**| Offset to consider in window of responses returned | [optional] [default to 0]

### Return type

[**InlineResponse2009**](InlineResponse2009.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## modifyTemplate

> TemplateResponse modifyTemplate(templateId, templateResponse)

Modify response template

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.TemplatesApi();
let templateId = 5bb89a7e3b18fb3d95495f2e; // String | Template ID
let templateResponse = new RasaXHttpApi.TemplateResponse(); // TemplateResponse | 
apiInstance.modifyTemplate(templateId, templateResponse, (error, data, response) => {
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
 **templateResponse** | [**TemplateResponse**](TemplateResponse.md)|  | 

### Return type

[**TemplateResponse**](TemplateResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## postTemplate

> TemplateResponse postTemplate(templateResponse)

Add to templates collection

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.TemplatesApi();
let templateResponse = new RasaXHttpApi.TemplateResponse(); // TemplateResponse | 
apiInstance.postTemplate(templateResponse, (error, data, response) => {
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
 **templateResponse** | [**TemplateResponse**](TemplateResponse.md)|  | 

### Return type

[**TemplateResponse**](TemplateResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

