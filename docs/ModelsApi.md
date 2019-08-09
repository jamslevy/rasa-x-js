# RasaXHttpApi.ModelsApi

All URIs are relative to *http://api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getModels**](ModelsApi.md#getModels) | **GET** /projects/{project_id}/models | Get a list of Rasa models
[**projectsProjectIdModelsModelDelete**](ModelsApi.md#projectsProjectIdModelsModelDelete) | **DELETE** /projects/{project_id}/models/{model} | Delete a Rasa Core model
[**projectsProjectIdModelsModelTagsTagDelete**](ModelsApi.md#projectsProjectIdModelsModelTagsTagDelete) | **DELETE** /projects/{project_id}/models/{model}/tags/{tag} | Delete a tag of a Rasa model
[**projectsProjectIdModelsModelTagsTagPut**](ModelsApi.md#projectsProjectIdModelsModelTagsTagPut) | **PUT** /projects/{project_id}/models/{model}/tags/{tag} | Tag a Rasa model
[**projectsProjectIdModelsPost**](ModelsApi.md#projectsProjectIdModelsPost) | **POST** /projects/{project_id}/models | Upload a zipped Rasa model
[**projectsProjectIdModelsTagsTagGet**](ModelsApi.md#projectsProjectIdModelsTagsTagGet) | **GET** /projects/{project_id}/models/tags/{tag} | Get a Rasa Core model with tag



## getModels

> [Model] getModels(projectId, opts)

Get a list of Rasa models

Returns a list of metadata on Rasa models. A Rasa model is a model combining a trained dialogue model with an NLU model.

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.ModelsApi();
let projectId = default; // String | Project ID
let opts = {
  'offset': 0, // Number | 
  'limit': 3.4 // Number | 
};
apiInstance.getModels(projectId, opts, (error, data, response) => {
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
 **offset** | **Number**|  | [optional] [default to 0]
 **limit** | **Number**|  | [optional] 

### Return type

[**[Model]**](Model.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## projectsProjectIdModelsModelDelete

> String projectsProjectIdModelsModelDelete(projectId, model)

Delete a Rasa Core model

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.ModelsApi();
let projectId = default; // String | Project ID
let model = "model_example"; // String | Model name
apiInstance.projectsProjectIdModelsModelDelete(projectId, model, (error, data, response) => {
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
 **model** | **String**| Model name | 

### Return type

**String**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: text/plain


## projectsProjectIdModelsModelTagsTagDelete

> String projectsProjectIdModelsModelTagsTagDelete(projectId, model, tag)

Delete a tag of a Rasa model

Rasa model tags can be deleted at this endpoint.

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.ModelsApi();
let projectId = default; // String | Project ID
let model = "model_example"; // String | Model name
let tag = "tag_example"; // String | Model tag
apiInstance.projectsProjectIdModelsModelTagsTagDelete(projectId, model, tag, (error, data, response) => {
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
 **model** | **String**| Model name | 
 **tag** | **String**| Model tag | 

### Return type

**String**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: text/plain


## projectsProjectIdModelsModelTagsTagPut

> String projectsProjectIdModelsModelTagsTagPut(projectId, model, tag)

Tag a Rasa model

This endpoint can be used to assign a tag to a Rasa model. The tag will be removed from any other model that might have it. The endpoint returns the assigned tag with status code 200.

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.ModelsApi();
let projectId = default; // String | Project ID
let model = "model_example"; // String | Model name
let tag = "tag_example"; // String | Model tag
apiInstance.projectsProjectIdModelsModelTagsTagPut(projectId, model, tag, (error, data, response) => {
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
 **model** | **String**| Model name | 
 **tag** | **String**| Model tag | 

### Return type

**String**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: text/plain


## projectsProjectIdModelsPost

> String projectsProjectIdModelsPost(projectId, opts)

Upload a zipped Rasa model

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.ModelsApi();
let projectId = default; // String | Project ID
let opts = {
  'body': null // Object | 
};
apiInstance.projectsProjectIdModelsPost(projectId, opts, (error, data, response) => {
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
 **body** | **Object**|  | [optional] 

### Return type

**String**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/gzip
- **Accept**: text/plain


## projectsProjectIdModelsTagsTagGet

> String projectsProjectIdModelsTagsTagGet(projectId, tag)

Get a Rasa Core model with tag

### Example

```javascript
import RasaXHttpApi from 'rasa_x_http_api';
let defaultClient = RasaXHttpApi.ApiClient.instance;
// Configure Bearer (JWT) access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new RasaXHttpApi.ModelsApi();
let projectId = default; // String | Project ID
let tag = "tag_example"; // String | Model tag
apiInstance.projectsProjectIdModelsTagsTagGet(projectId, tag, (error, data, response) => {
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
 **tag** | **String**| Model tag | 

### Return type

**String**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/octet-stream

